---
description: 源对象说明符。 图像、SVG和ICC配置文件对象可以指定为图像目录条目或相对文件路径
solution: Experience Manager
title: 对象
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# 对象{#object}

源对象说明符。 图像、SVG和ICC配置文件对象可以指定为图像目录条目或相对文件路径

`*`对象`*[/]{[ *`rootId`*/] *`objId`*}| *`路径`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>图像目录的名称( <span class="codeph"> 属性：:RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主目录或默认图像目录中图像、SVG、模板或ICC配置文件记录的id </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路径 </span> </span> </p> </td> 
  <td class="stentry"> <p>相对图像、蒙版或ICC配置文件文件路径和名称 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 对象 </span> </span> </p> </td> 
  <td class="stentry"> <p>可能出现在主URL路径中，也可能出现在 <span class="codeph"> src= </span>, <span class="codeph"> 掩码= </span>或 <span class="codeph"> icc= </span> 命令 </p> </td> 
 </tr> 
</table>

*`rootId`* 标识图像目录。 (请参阅 [图像目录](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) () 如果 *`rootId`* 在URL路径中指定，则该目录将变为 *主目录* 请求。 否则，将使用默认目录作为主目录。 可在同一请求中使用多个不同的图像目录。

服务器最初假定 *`rootId`* 在 `src=`, `mask=`和 `icc=` 命令和将尝试在主目录中查找目录条目。 实际上，服务器会尝试使用 *`object`* 字符串 *`objId.`*

如果找到目录条目，则使用；否则，服务器将尝试匹配 *`rootId`* 图像目录的子目录。 如果识别了目录，则会搜索该目录 *`objId`*. 如果找到和条目，则使用。

否则， *`object`* 假定为显式文件路径。 在这种情况下，如果 `attribute::FullMatch` 在主目录中设置，则将忽略此对象的目录，并改为使用默认目录。 如果 `attribute::FullMatch` 未设置，则将使用主目录进行进一步处理。

两者兼有 *`rootId`* 和 *`objId`* 区分大小写。 *`path`* 仅在UNIX上区分大小写。

如果前导 `/` 指定，则会搜索默认目录而不是主目录。 当显式路径需要 `default::RootPath` 而不是主目录的 `attribute::RootPath`，但也可用于获取对默认目录中条目的访问权限，否则，这些条目将被主目录中的条目覆盖。

请参阅 *管理内容* 在 *服务器配置指南* 有关如何 *`path`* 被转换为物理文件路径。

>[!NOTE]
>
>中不允许使用逗号“，”字符 *`object.`*

## 支持的图像文件格式 {#section-12c85aead78e4f759856ca9ff10637d7}

请参阅IC（图像转换器）实用程序的说明，以获取支持文件格式的完整列表。

当使用Dynamic Media金字塔TIFF(PTIF)多分辨率格式时，需要多种不同分辨率的图像数据的应用程序将发挥最佳性能。 IC实用程序用于从任何支持的图像格式创建PTIF图像。

## 示例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**在两个不同的图像目录中访问图像和ICC配置文件**

检索图像“ [!DNL myImage]在标识为“ [!DNL myCatalog]“ ”并附加ICC配置文件“ [!DNL sRGB]“ ”位于名为“ ”的图像目录中 [!DNL myProfiles]&#39;:

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用具有分层的单个图像目录

**构建一个由三个层组成的简单复合图像，所有这些层均从“ [!DNL myCatalog]&#39;:**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接访问图像文件，同时仍使用目录提供属性**

访问 [!DNL my/image/path/myImage.tif]，使用中配置的默认jpg属性 `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另请参阅 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC实用程序](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [掩码=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [属性：:FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
