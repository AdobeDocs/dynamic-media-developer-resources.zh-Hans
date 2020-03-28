---
description: 图像服务提供了一种将外部对象ID转换为特定于区域设置的对象（目录）ID的机制。 主应用程序用于提供在多个区域设置之间共享的区域设置特定内容和内容，而客户端应用程序无需了解区域设置特定的对象ID。
seo-description: 图像服务提供了一种将外部对象ID转换为特定于区域设置的对象（目录）ID的机制。 主应用程序用于提供在多个区域设置之间共享的区域设置特定内容和内容，而客户端应用程序无需了解区域设置特定的对象ID。
seo-title: 对象ID转换
solution: Experience Manager
title: 对象ID转换
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b4c2f44-033a-428a-b505-af389865c70a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 对象ID转换{#object-id-translation}

图像服务提供了一种将外部对象ID转换为特定于区域设置的对象（目录）ID的机制。 主应用程序用于提供在多个区域设置之间共享的区域设置特定内容和内容，而客户端应用程序无需了解区域设置特定的对象ID。

只能使用全局对象ID编写应用程序，图像服务将自动替换区域设置特定的图像和其他可用内容。

在图 *`locale`* 像服务请求中使用命令指定 `locale=` 该值。

>[!NOTE]
>
>对象ID转换仅适用于基于目录的图像服务使用。 文件名无法翻译。

## 范围 {#section-66fcd5bd467c4eeaa1574583cbe9756d}

对图像、SVG和静态内容目录中条目的所有引用都将用于翻译字体，而ICC用户档案引用不会进行翻译。 除了和的路 *`object`* 径之外，这些命令 [!DNL /is/image] 和 [!DNL /is/static requests]目录属性还受ID转换的约束： `src=`、 `mask=`、 `template=`、 `defaultImage=`和 `attribute::DefaultImage``attribute::Watermark`。

## ID转换映射 {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` 定义服务器用来确定本地化内容的ID的规则，该规则作为通用对象ID和值的输入给 `locale=` 定。

`attribute::LocaleMap` 由一列表输入区域设 *置* (与指定的值匹配 `locale=`)组成，每个区域设置都没有或更多输出区域设置后缀( ` *`locSuffixes`*`)。

例如， `attribute::LocaleMap` 可能如下所示：

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

请求将 `/is/image/myCat/myImg?locale=de_de` 返回与目录条目关联的图像 `myCat/myImg_D` （假定存在此类目录条目）。

有关详细信息，请参 `attribute::LocaleMap` 阅的说明。

## 翻译过程 {#section-1f64db17e9f644d88e09853670e14a16}

在上面的示例中，服务器首先在ID转 *`locale`* 换图 `de_de`中查找“ ”。 然后，它将迭代与 *`locSuffixes`* 此条目关联的条目——在本例中为“ `_D`”和“”（空后缀）。 对于每次迭代，后缀都会附加到图像ID和测试在目录中存在的结果ID上。 如果找到该目录条目，则使用该目录条目，否则将测试下一个条目。 在此示例中，将选中以下条目： `myCat/myImg_D`和 `myCat/myImg`。 如果未找到匹配项，则服务器会返回错误或默认图像（如果已配置）。

## 未知区域设置 {#section-b2f3c83f2dc845d69b5908107b775537}

在上例中，包 `attribute::LocaleMap` 括一个空，它定义默认的翻译规则，用于未知 *`locale`*`locale=` 值（即未在翻译图中明确列出的值）。 如果此翻译图已应用于请 `/is/image/myCat/myImg?locale=ja`求，它将解析 `myCat/myImg_E`为（如果存在）或其他 `myCat/myImg`。

如果翻译图未指定默认的翻译规则，则对于具有未知值的所有请求将返回一个 `locale=` 错误。

## 示例 {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**多层查找**

通常，最好将区域设置（例如，欧洲、中东、北美）分组，以符合区域标准。 这可以通过多层查找来实现。

在此示例中，我们希望支持用于西部和中东用途的集合。 这两个集合都基于通用图像集合，而且都添加或修改某些图像。Both collections are then further refined for specific locales ( `m1`, `m2` for two middle-eastern variants, and `w1`, `w2`, and `w3` for three Western locales), except that images are shared for `w1` and `w3`. 未知区域设置仅映射到通用集合，而且无法访问区域设置特定的图像。

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

下表说明了将考虑哪些目录条目以及它们作为通用输入ID的考虑顺序 `myImg`:

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

某些图像命名约定可能在内部不支持通用图像ID。 请求中的通用ID必须始终映射到目录中的特定ID;通常，具体的特定ID可能未知。

在本例中，所有语言的图像都可能 `_1`有、 `_2`或后 `_3` 缀。 特定于法语区域设置的图像可能 `_22` 具有 `_23` 或后缀，而特定于德语区域设置的图像可能具有 `_470` 或后 `_480` 缀。

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

下表说明了哪些目录条目被考虑，以及它们被视为通用输入ID的顺序 `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>要搜索的输出ID</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2,myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有其他 </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 另请参阅 {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute:::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
