---
description: 图像服务提供了一种将外部对象ID转换为特定于区域设置的对象（目录）ID的机制。 主要应用程序用于提供特定于区域设置的内容以及在多个区域设置之间共享的内容，而无需客户端应用程序知道特定于区域设置的对象ID。
solution: Experience Manager
title: 对象标识转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---

# 对象标识转换{#object-id-translation}

图像服务提供了一种将外部对象ID转换为特定于区域设置的对象（目录）ID的机制。 主要应用程序用于提供特定于区域设置的内容以及在多个区域设置之间共享的内容，而无需客户端应用程序知道特定于区域设置的对象ID。

应用程序只能使用全局对象ID进行编写，并且图像服务会自动替换特定于区域设置的图像和其他内容（如果可用）。

使用&#x200B;*`locale`*&#x200B;命令在图像服务请求中指定`locale=`。

>[!NOTE]
>
>对象ID转换仅适用于基于目录的图像服务使用。 无法翻译文件名。

## 范围 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

对图像、SVG和静态内容目录中的条目的所有引用都被视为翻译字体，并且ICC配置文件引用不会进行翻译。 除了&#x200B;*`object`*&#x200B;和[!DNL /is/image]路径中的[!DNL /is/static requests]之外，这些命令和目录属性还受ID转换的影响： `src=`、`mask=`、`template=`、`defaultImage=`、`attribute::DefaultImage`和`attribute::Watermark`。

## ID转换映射 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap`定义服务器用于确定本地化内容的ID的规则，作为输入提供通用对象ID和`locale=`值。

`attribute::LocaleMap`由输入&#x200B;*区域设置*&#x200B;的列表组成（与使用`locale=`指定的值匹配），每个区域设置后缀都不包含或超过输出区域设置后缀(`*`locSuffixes`*`)。

例如，`attribute::LocaleMap`可能如下所示：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

请求`/is/image/myCat/myImg?locale=de_de`将返回与目录条目`myCat/myImg_D`关联的图像（假设存在此类目录条目）。

有关详细信息，请参阅`attribute::LocaleMap`的说明。

## 翻译过程 {#section-1f64db17e9f644d88e09853670e14a16}

根据以上示例，服务器首先在ID转换映射中查找&#x200B;*`locale`*“`de_de`”。 然后，它会迭代与此条目关联的&#x200B;*`locSuffixes`*，在本例中为“`_D`”和“”（后缀为空）。 对于每次迭代，后缀都会附加到图像ID中，并且生成的ID将进行目录中存在的测试。 如果找到，则使用该目录条目，否则测试下一个目录条目。 在本例中，这些条目被选中： `myCat/myImg_D`和`myCat/myImg`。 如果未找到匹配项，则服务器会返回错误或默认图像（如果已配置）。

## 未知区域设置 {#section-b2f3c83f2dc845d69b5908107b775537}

在上例中，`attribute::LocaleMap`包含一个空的&#x200B;*`locale`*，它定义了用于未知`locale=`值（即未在翻译映射中显式列出的值）的默认翻译规则。 如果此翻译映射应用于请求`/is/image/myCat/myImg?locale=ja`，它将解析为`myCat/myImg_E`（如果存在），否则`myCat/myImg`。

如果翻译映射未指定默认翻译规则，则将为具有未知`locale=`值的所有请求返回错误。

## 示例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多层查找**

通常，将区域设置分组（例如，欧洲、中东、北美）以符合区域标准是值得的。 这可以通过多层查找来实现。

对于此示例，我们希望支持收藏集供西方和中东使用。 这两个集合都基于通用图像集合，而且都添加或修改某些图像。然后针对特定区域设置进一步优化这两个集合（针对两个中东变体为`m1`、`m2`，针对三个西方区域设置为`w1`、`w2`和`w3`），但针对`w1`和`w3`共享图像的情况除外。 未知区域设置仅映射到通用收藏集，无法访问特定于区域设置的图像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表说明了考虑的目录条目，以及考虑通用输入ID `myImg`的目录条目的顺序：

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>区域设置</i> </b> </th> 
   <th class="entry"> <b>要搜索的目录ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1，w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W， myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2， myImg-W， myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1、myImg-M、myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2， myImg-M， myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**搜索特定ID**

某些图像命名惯例在内部可能不支持通用图像ID。 请求中的通用ID必须始终映射到目录中的特定ID；通常，确切的特定ID可能未知。

对于此示例，所有语言的图像可能具有`_1`、`_2`或`_3`后缀。 特定于法语区域设置的图像可能具有`_22`或`_23`后缀，而特定于德语区域设置的图像可能具有`_470`或`_480`后缀。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表说明了考虑的目录条目，以及考虑通用输入ID `myImg`的目录条目的顺序：

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>区域设置</i> </b> </th> 
   <th class="entry"> <b>要搜索的输出ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">的</span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22、myImg_23、myImg_1、myImg_2、myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>，<span class="codeph"> de_at </span>，<span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470、myImg_480、myImg_1、myImg_2、myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1， myImg_2， myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另请参阅 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ， [attribute：：DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
