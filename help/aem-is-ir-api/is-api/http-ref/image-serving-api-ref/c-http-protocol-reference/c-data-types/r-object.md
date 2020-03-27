---
description: 源对象说明符。 图像、SVG和ICC用户档案对象可指定为图像目录条目或相对文件路径
seo-description: 源对象说明符。 图像、SVG和ICC用户档案对象可指定为图像目录条目或相对文件路径
seo-title: 对象
solution: Experience Manager
title: 对象
topic: Scene7 Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# object{#object}

源对象说明符。 图像、SVG和ICC用户档案对象可指定为图像目录条目或相对文件路径

` *``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span></span> </p> </td> 
  <td class="stentry"> <p>图像目录的名称( <span class="codeph"> 属性：:RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId </span></span> </p> </td> 
  <td class="stentry"> <p>指定图像目录、主图像目录或默认图像目录中的图像ID、SVG、模板或ICC用户档案记录 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 路径 </span></span> </p> </td> 
  <td class="stentry"> <p>相对图像、蒙版或ICC用户档案文件路径和名称 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 对象 </span></span> </p> </td> 
  <td class="stentry"> <p>可能出现在主URL路径中，或出现在 <span class="codeph"> src=、 </span><span class="codeph"> mask= </span>或 <span class="codeph"> icc=命 </span> 令中 </p> </td> 
 </tr> 
</table>

*`rootId`* 标识图像目录。 (See [Image Catalog](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) for details.) 如果 *`rootId`* 在URL路径中指定了该目录，则该目录将成 *为此请求的主目录* 。 否则，默认目录将用作主目录。 同一请求中可以使用多个不同的图像目录。

服务器最初假定 *`rootId`* 在、 `src=``mask=`和命令中省略，并 `icc=` 且将尝试在主目录中查找目录条目。 实际上，服务器会尝试将整个字符串 *`object`* 用作 *`objId.`*

如果找到目录条目，则使用它；否则，服务器下次尝试匹配图 *`rootId`* 像目录。 如果识别了目录，则会搜索该目录 *`objId`*。 如果找到并输入，则使用它。

否则， *`object`* 假定为显式文件路径。 在这种情况下，如 `attribute::FullMatch` 果在主目录中设置，则忽略此对象的目录，而改用默认目录。 如果 `attribute::FullMatch` 未设置，则主目录用于进一步处理。

和 *`rootId`* 均 *`objId`* 区分大小写。 *`path`* 仅在UNIX上区分大小写。

如果指定了前导“/”，则将搜索默认目录而不是主目录。 当显式路径需要而非主目录的条目时，这 `default::RootPath` 一功能主要有用 `attribute::RootPath`，但也可以用于访问默认目录中的条目，否则这些条目将被主目录中的条目覆盖。

有关如何将 *内容转换为物理文件路径的详细信息，请参阅《服务器配置指南* 》中 ***`path`* 的“管理内容”。

>[!NOTE]
>
>不允许在 *`object.`*

## 支持的图像文件格式 {#section-12c85aead78e4f759856ca9ff10637d7}

有关所支持文件格式的完整列表，请参阅IC（图像转换器）实用程序的说明。

使用Scene7金字塔TIFF(PTIF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最佳。 IC实用程序用于根据任何支持的图像格式创建PTIF图像。

## 示例 {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**在两个不同的图像目录中访问图像和ICC用户档案**

在标识为“ [!DNL myImage]”的图像目录中检索图像“ [!DNL myCatalog]”，并附加位于名为“ [!DNL sRGB]”的图像目录中的ICC用户档案“ [!DNL myProfiles]”:

` http:// *`伺服器`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

使用具有分层的单个图像目录

**构建一个由三个图层组成的简单复合图像，所有图层都从“[!DNL myCatalog]”检索：**

` http:// *`伺服器`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**在仍使用目录提供属性的同时直接访问图像文件**

访 [!DNL my/image/path/myImage.tif]问，使用在以下位置配置的默认jpg属性 `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## 另请参阅 {#section-b6eccefad63f441d922699c4aba58fc9}

[IC实用程序](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [属性：:FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
