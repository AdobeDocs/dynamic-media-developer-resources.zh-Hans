---
description: 源对象说明符。 可以将图像、SVG和ICC配置文件对象指定为图像目录条目或相对文件路径
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

源对象说明符。 可以将图像、SVG和ICC配置文件对象指定为图像目录条目或相对文件路径

`*`对象`*[/]{[ *`rootId`*/] *`objId`*}| *`路径`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>图像目录的名称( <span class="codeph"> attribute：：RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>指定、主或默认图像目录中的图像、SVG、模板或ICC配置文件记录的ID </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路径 </span> </span> </p> </td> 
  <td class="stentry"> <p>相对图像、蒙版或ICC配置文件文件路径和名称 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 对象 </span> </span> </p> </td> 
  <td class="stentry"> <p>可能出现在主URL路径中，也可能出现在 <span class="codeph"> src= </span>， <span class="codeph"> 蒙版= </span>，或 <span class="codeph"> icc= </span> 命令 </p> </td> 
 </tr> 
</table>

*`rootId`* 标识图像目录。 (请参阅 [图像目录](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 了解详细信息。) 如果 *`rootId`* 在URL路径中指定，则该目录将变为 *主目录* 请求的。 否则，将默认目录用作主目录。 同一请求中可以使用多个不同的图像目录。

服务器最初假设 *`rootId`* 中省略 `src=`， `mask=`、和 `icc=` 命令，并将尝试在主目录中找到目录条目。 实际上，服务器尝试使用整个 *`object`* 字符串为 *`objId.`*

如果找到目录条目，则使用该条目；否则，服务器下一步将尝试匹配 *`rootId`* 图像目录的。 如果标识了目录，则搜索该目录 *`objId`*. 如果找到和条目，则使用它。

否则， *`object`* 假定为显式文件路径。 在这种情况下，如果 `attribute::FullMatch` 在主目录中设置，则会忽略此对象的目录，而改用默认目录。 如果 `attribute::FullMatch` 未设置，则使用主目录进行进一步处理。

两者 *`rootId`* 和 *`objId`* 区分大小写。 *`path`* 仅在UNIX上区分大小写。

如果行距 `/` 指定时，将搜索默认目录而不是主目录。 当显式路径需要 `default::RootPath` 而不是主目录的 `attribute::RootPath`，也可用于获取对默认目录中条目的访问权限，否则这些条目将被主目录中的条目覆盖。

请参阅 *管理内容* 在 *服务器配置指南* 了解关于如何操作的详细信息 *`path`* 将转换为物理文件路径。

>[!NOTE]
>
>中不允许使用逗号“，”字符 *`object.`*

## 支持的图像文件格式 {#section-12c85aead78e4f759856ca9ff10637d7}

有关支持的文件格式的完整列表，请参阅IC（图像转换器）实用程序的说明。

当使用Dynamic Media金字塔TIFF(PTIF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序将获得最佳性能。 IC实用程序用于从任何支持的图像格式创建PTIF图像。

## 示例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**访问两个不同图像目录中的图像和ICC配置文件**

检索图像&#39; [!DNL myImage]图像目录中的“ ”标识为“ [!DNL myCatalog]&#39;并附加ICC配置文件&#39; [!DNL sRGB]&#39;位于名为的图像目录中&#39; [!DNL myProfiles]&#39;：

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用具有分层的单个图像目录

**构建包含三个层的简单复合图像，所有层均检索自“ [!DNL myCatalog]&#39;：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**直接访问图像文件，同时仍使用目录来提供属性**

访问 [!DNL my/image/path/myImage.tif]，使用在中配置的默认jpg属性 `myImageCatalog`：

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另请参阅 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC实用程序](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)， [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)， [蒙版=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [attribute：：FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
