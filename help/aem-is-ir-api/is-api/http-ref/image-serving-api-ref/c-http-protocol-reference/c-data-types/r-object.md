---
description: 源对象说明符。 图像、SVG和ICC用户档案对象可指定为图像目录条目或相对文件路径
seo-description: 源对象说明符。 图像、SVG和ICC用户档案对象可指定为图像目录条目或相对文件路径
seo-title: 对象
solution: Experience Manager
title: 对象
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 1%

---


# object{#object}

源对象说明符。 图像、SVG和ICC用户档案对象可指定为图像目录条目或相对文件路径

`*``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>图像目录的名称（<span class="codeph">属性：:RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主或默认图像目录中的图像、SVG、模板或ICC用户档案记录的id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路径  </span> </span> </p> </td> 
  <td class="stentry"> <p>相对图像、蒙版或ICC用户档案文件路径和名称 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 对象  </span> </span> </p> </td> 
  <td class="stentry"> <p>可能出现在主URL路径中，或出现在<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>或<span class="codeph"> icc= </span>命令中 </p> </td> 
 </tr> 
</table>

*`rootId`* 标识图像目录。（有关详细信息，请参阅[图像目录](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)。） 如果在URL路径中指定了&#x200B;*`rootId`*，则该目录将成为此请求的&#x200B;*主目录*。 否则，默认目录将用作主目录。 可以在同一请求中使用多个不同的图像目录。

服务器最初假定`src=`、`mask=`和`icc=`命令中省略&#x200B;*`rootId`*，并将尝试在主目录中查找目录条目。 有效地，服务器会尝试将整个&#x200B;*`object`*&#x200B;字符串用作&#x200B;*`objId.`*

如果找到目录条目，则使用它；否则，服务器下次尝试匹配图像目录的&#x200B;*`rootId`*。 如果标识了目录，则搜索&#x200B;*`objId`*。 如果找到并输入，则使用它。

否则，假定&#x200B;*`object`*&#x200B;为显式文件路径。 在这种情况下，如果在主目录中设置`attribute::FullMatch`，则忽略此对象的目录，而改用默认目录。 如果未设置`attribute::FullMatch`，则使用主目录进一步处理。

*`rootId`*&#x200B;和&#x200B;*`objId`*&#x200B;都区分大小写。 *`path`* 仅在UNIX上区分大小写。

如果指定了前导“/”，则将搜索默认目录，而不是主目录。 当显式路径需要`default::RootPath`而非主目录的`attribute::RootPath`时，此功能非常有用，但也可用于访问默认目录中的条目，否则这些条目将被主目录中的条目覆盖。

有关如何将&#x200B;*`path`*&#x200B;转换为物理文件路径的详细信息，请参阅&#x200B;*服务器配置指南*&#x200B;中的&#x200B;*管理内容*。

>[!NOTE]
>
>*`object.`*&#x200B;中不允许使用逗号“，”字符

## 支持的图像文件格式{#section-12c85aead78e4f759856ca9ff10637d7}

有关所支持文件格式的完整列表，请参阅IC（图像转换器）实用程序的说明。

使用Dynamic Media金字塔TIFF(PTIF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最好。 IC实用程序用于根据任何支持的图像格式创建PTIF图像。

## 示例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**在两个不同的图像目录中访问图像和ICC用户档案**

在标识为“ [!DNL myCatalog]”的图像目录中检索图像“ [!DNL myImage]”，并附加名为“ [!DNL myProfiles]”的图像目录中的ICC用户档案“ [!DNL sRGB]”：

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用具有分层的单个图像目录

**构建一个由三个图层组成的简单复合图像，所有图层均从“” [!DNL myCatalog]中检索：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接访问图像文件，同时仍使用目录提供属性**

使用在`myImageCatalog`中配置的默认jpg属性访问[!DNL my/image/path/myImage.tif]:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另请参阅 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC实用程](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)序， [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [属性：:FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
