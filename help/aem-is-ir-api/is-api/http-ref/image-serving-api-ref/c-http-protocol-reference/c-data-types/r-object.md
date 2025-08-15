---
description: Source对象说明符。 可以将图像、SVG和ICC配置文件对象指定为图像目录条目或相对文件路径
solution: Experience Manager
title: 对象
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# 对象{#object}

Source对象说明符。 可以将图像、SVG和ICC配置文件对象指定为图像目录条目或相对文件路径

`*`对象`*[/]{[ *`rootId`*/] *`objId`*}| *`路径`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>图像目录的名称（<span class="codeph">属性：：RootId </span>） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主或默认图像目录中的图像、SVG、模板或ICC配置文件记录的ID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">路径</span> </span> </p> </td> 
  <td class="stentry"> <p>相对图像、蒙版或ICC配置文件文件路径和名称 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">对象</span> </span> </p> </td> 
  <td class="stentry"> <p>可能在主URL路径中或<span class="codeph"> src= </span>、<span class="codeph"> mask= </span>或<span class="codeph"> icc= </span>命令中出现 </p> </td> 
 </tr> 
</table>

*`rootId`*&#x200B;标识图像目录。 （有关详细信息，请参阅[图像目录](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)。） 如果在URL路径中指定了&#x200B;*`rootId`*，则该目录将成为此请求的&#x200B;*主目录*。 否则，将默认目录用作主目录。 同一请求中可以使用多个不同的图像目录。

服务器最初假设&#x200B;*`rootId`*、`src=`和`mask=`命令中省略`icc=`，并尝试在主目录中找到目录条目。 实际上，服务器尝试将整个&#x200B;*`object`*&#x200B;字符串用作&#x200B;*`objId.`*

如果找到目录条目，则使用该条目；否则，服务器下一步将尝试匹配图像目录的&#x200B;*`rootId`*。 如果标识了目录，则会搜索该目录&#x200B;*`objId`*。 如果找到和条目，则使用它。

否则，*`object`*&#x200B;被假定为显式文件路径。 在本例中，如果在主目录中设置`attribute::FullMatch`，则忽略此对象的目录，并改用默认目录。 如果未设置`attribute::FullMatch`，则使用主目录进行进一步处理。

*`rootId`*&#x200B;和&#x200B;*`objId`*&#x200B;都区分大小写。 *`path`*&#x200B;仅在UNIX上区分大小写。

如果指定了前导`/`，则搜索默认目录而不是主目录。 当显式路径需要`default::RootPath`而不是主目录的`attribute::RootPath`时，这非常有用，但也可以用于获取对默认目录中的条目的访问权限，否则，这些条目将被主目录中的条目覆盖。

有关如何将&#x200B;*转换为物理文件路径的详细信息，请参阅*&#x200B;服务器配置指南&#x200B;*中的*&#x200B;管理内容&#x200B;*`path`*。

>[!NOTE]
>
>*`object.`*&#x200B;中不允许使用逗号“，”字符

## 支持的图像文件格式 {#section-12c85aead78e4f759856ca9ff10637d7}

有关支持的文件格式的完整列表，请参阅IC（图像转换器）实用程序的说明。

当使用Dynamic Media金字塔TIFF (PTIF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最佳。 IC实用程序用于从任何支持的图像格式创建PTIF图像。

## 示例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**访问两个不同图像目录中的图像和ICC配置文件**

检索标识为“[!DNL myImage]”的图像目录中的图像“[!DNL myCatalog]”，并附加位于名为“[!DNL sRGB]”的图像目录中的ICC配置文件“[!DNL myProfiles]”：

` http:// *`服务器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

将单个图像目录与分层结合使用

**构建包含三个层的简单复合图像，所有层均从“[!DNL myCatalog]”中检索：**

` http:// *`服务器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接访问图像文件，同时仍使用目录提供属性**

使用[!DNL my/image/path/myImage.tif]中配置的默认jpg属性访问`myImageCatalog`：

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另请参阅 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC实用工具](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)，[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)，[掩码=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)，[属性：：FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
