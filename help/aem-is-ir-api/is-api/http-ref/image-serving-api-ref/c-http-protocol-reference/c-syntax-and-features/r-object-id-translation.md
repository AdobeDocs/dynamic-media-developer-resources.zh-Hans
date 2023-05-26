---
description: 图像服务提供了一种将外部对象ID转换为特定于区域设置的对象（目录）ID的机制。 主要应用程序用于提供特定于区域设置的内容和在多个区域设置之间共享的内容，而无需客户端应用程序知道特定于区域设置的对象ID。
solution: Experience Manager
title: 对象标识转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# 对象标识转换{#object-id-translation}

图像服务提供了一种将外部对象ID转换为特定于区域设置的对象（目录）ID的机制。 主要应用程序用于提供特定于区域设置的内容和在多个区域设置之间共享的内容，而无需客户端应用程序知道特定于区域设置的对象ID。

应用程序只能使用全局对象ID进行编写，图像服务将自动替换特定于区域设置的图像和其他内容（如果可用）。

此 *`locale`* 在图像服务请求中通过 `locale=` 命令。

>[!NOTE]
>
>对象ID转换仅适用于基于目录的图像服务使用。 无法翻译文件名。

## 范围 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

对于翻译字体，图像、SVG和静态内容目录中对条目的所有引用都将被考虑在内，并且ICC配置文件引用不会被翻译。 除了 *`object`* 在路径 [!DNL /is/image] 和 [!DNL /is/static requests]，以下命令和目录属性将受ID转换的约束： `src=`， `mask=`， `template=`， `defaultImage=`， `attribute::DefaultImage`、和 `attribute::Watermark`.

## ID转换映射 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 定义服务器用于确定本地化内容ID的规则，在输入通用对象ID和 `locale=` 值。

`attribute::LocaleMap` 由输入列表组成 *区域设置* (匹配指定的值 `locale=`)，每个区域设置后缀都不包含或更多( `*`locSuffixes`*`)。

例如， `attribute::LocaleMap` 可能如下所示：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

请求 `/is/image/myCat/myImg?locale=de_de` 将返回与目录条目关联的图像 `myCat/myImg_D` （假设存在此类目录条目）。

请参阅 `attribute::LocaleMap` 了解详细信息。

## 翻译过程 {#section-1f64db17e9f644d88e09853670e14a16}

根据以上示例，服务器首先查找 *`locale`* ” `de_de`”在ID转换映射中。 然后，它将遍历以下内容： *`locSuffixes`* 与此条目相关联，在本例中为“ `_D`“”和“”（空后缀）。 对于每次迭代，后缀都会附加到图像ID中，并且生成的ID会测试在目录中的存在。 如果找到，则使用该目录条目，否则测试下一个目录条目。 在本例中，将检查以下条目： `myCat/myImg_D`、和 `myCat/myImg`. 如果未找到匹配项，则服务器会返回一个错误或默认映像（如果已如此配置）。

## 未知区域设置 {#section-b2f3c83f2dc845d69b5908107b775537}

在上例中， `attribute::LocaleMap` 包含空 *`locale`* 用于定义默认翻译规则，用于未知 `locale=` 值（即未在翻译映射中明确列出的值）。 如果此翻译映射应用于请求 `/is/image/myCat/myImg?locale=ja`，它将 `myCat/myImg_E`，如果存在，或者 `myCat/myImg`.

如果翻译映射未指定默认翻译规则，则会为所有未知请求返回错误 `locale=` 值。

## 示例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多层查找**

通常，最好将区域设置分组（例如，欧洲、中东、北美地区）以满足区域标准。 这可以通过多层查找来实现。

对于此示例，我们希望支持收藏集供西方和中东使用。 这两个集合都基于通用图像集合，而且都添加或修改某些图像。然后，针对特定区域设置( `m1`， `m2` 两个中东变种的，以及 `w1`， `w2`、和 `w3` （对于三种西方区域设置），但图像共享用于 `w1` 和 `w3`. 未知区域设置仅映射到通用集合，而且无法访问区域设置特定的图像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表说明了考虑哪些目录条目，以及考虑它们作为通用输入ID的顺序 `myImg`：

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>要搜索的目录ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**搜索特定ID**

某些图像命名惯例在内部可能不支持通用图像ID。 请求中的通用ID必须始终映射到目录中的特定ID；通常可能不知道确切的特定ID。

在本例中，所有语言的图像可能都有 `_1`， `_2`，或 `_3` 后缀。 特定于法语区域设置的图像可能具有 `_22` 或 `_23` 后缀和特定于德语区域设置的图像可能具有 `_470` 或 `_480` 后缀。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表说明了考虑哪些目录条目，以及考虑它们作为通用输入ID的顺序 `myImg`：

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>要搜索的输出标识</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>， <span class="codeph"> de_at </span>， <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另请参阅 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute：：LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ， [attribute：：DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b)， [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb)， [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
