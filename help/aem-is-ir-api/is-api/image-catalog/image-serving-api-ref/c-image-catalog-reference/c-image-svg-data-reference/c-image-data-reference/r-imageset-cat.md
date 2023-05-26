---
description: 图像集数据。 提供了一种机制，用于定义Dynamic Media查看器使用的已排序图像集和控制属性。
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---

# ImageSet{#imageset}

图像集数据。 提供了一种机制，用于定义Dynamic Media查看器使用的已排序图像集和控制属性。

图像集由以逗号分隔的已排序项目列表组成，每个项目均由一个或多个子项目（图像ID、样本ID、媒体文件路径、标签等）组成，并以分号和/或冒号分隔。

大括号 `{ }` 和圆括号 `( )` 可用于分隔某些内容（如颜色值）或指示嵌套集。 使用此方式的大括号或圆括号不能进行编码，必须始终显示为匹配对，否则将发生目录分析错误。

>[!NOTE]
>
>以下字符用作集分隔符，当它们作为id或字符串值的一部分显示在集中时，必须进行HTTP编码：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



有关图像集的结构和使用的其他详细信息，请参阅图像服务查看器文档。

服务器会返回此字段的内容，而不进行修改以响应 `req=imageset` 请求。

## 标准集 {#section-5ecc8ffee7224668b63f601383665564}

图像服务本身支持以下集定义，对某些查看器的访问涉及服务器端解析、验证和处理集。 可以通过指定中的相应值来标识每个集类型 `catalog::AssetType`.

**基本样本集**

基本样本集中的每个项目均由对图像记录的引用和用作样本的图像记录的可选单独引用组成。

| `*`basicSwatchSet`*` | `*`样本项目`*&#42;[',' *`样本项目`*]` |
|---|---|
| `*`样本项目`*` | `*`imageId`*[';' *`色板`*]` |
| `*`色板`*` | `*`样本ID`*|solidColorSpecifier` |
| `*`imageId`*` | IS图像引用（目录/ID） |
| `*`样本ID`*` | IS图像引用（目录/ID） |
| `*`纯色说明符`*` | ` '{0x' *`rrrggbb`* [ *`标签`*]'}'` |
| `*`rrrggbb`*` | 纯色色板的6位十六进制RGB色值 |
| `*`label`*` | 纯色样本的可选文本标签 |

**分层样本集**

分层样本集中的每个项目均可由基本样本项目或样本集记录的引用组成（此类项目需要样本）。

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`样本项目`* | { *`basicSwatchSetId`* ';' *`色板`* }` |
| `*`basicSwatchSetId`*` | 对定义基本样本集的目录记录的IS引用（目录/id） |

**基本旋转集**

基本旋转集由图像ID的简单列表组成。

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**二维旋转集**

二维旋转集中的每个项目可以由一个简单图像、对基本旋转集的引用或由大括号分隔的线内基本旋转集组成。 可以使用圆括号代替大括号。

| `*`2dSpinItem`*` | `*`2d旋转集`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`基本旋转集`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | 对定义基本旋转集的目录记录的IS引用（目录/id） |

**页面集**

页面集中的每个项目最多可包含三个用冒号分隔的页面图像。

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**媒体集**

媒体集中的每个项目都可以由图像、基本样本集、分层样本集、基本旋转集、二维旋转集、页面集或视频资产组成。 每个媒体集项目也可以包含可选的样本和类型标识符。

| `*`mediaSet`*` | `*`项目`* &#42;[ , *`项目`* ]` |
|---|---|
| `*`项目`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`保留`* ] ] ]` |
| `*`videoItem`*` | `*`视频`* ; *`样本ID`*` |
| `*`recutItem`*` | `*`剪辑`* ; *`样本ID`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`样本ID`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`样本ID`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`样本ID`*` | IS图像id |
| `*`视频`*` | 视频/动画文件路径或静态目录ID |
| `*`剪辑`*` | 剪辑定义XML文件路径或静态目录ID |
| `*`imageId`*` | IS图像id |
| `*`setId`*` | 对图像、旋转或ecatalog集的IS引用 |
| `*`inlineSet`*` | 内联图像、旋转或ecatalog集 |
| `*`已保留`*` | 保留供将来使用 |

**Video Sets**

视频集由视频ID的简单列表组成，其中每个ID都引用静态内容目录中的一个条目。

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## 属性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文本字符串。 逗号分隔的列表 `catalog::Id` 值、绝对图像服务器文件路径或相对于 `attribute::RootPath`. 同一图像可在集中被多次引用。 定义目录记录可出现在集合的任何位置。

此字段参与文本字符串本地化。 除此之外 *`label`* 字符串（的一部分） *`solidColorSpecifier`*)如果所有分隔字段至少包含一个“ `^loc=…^`&#39;本地化令牌。 请参阅 [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 在 *HTTP协议参考* 了解详细信息。

## 默认 {#section-c3a60e360393478284f0f2d2da5b963b}

无。

## 另请参阅 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ， [attribute：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)， [对象ID转换](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ， [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) ，图像服务查看器文档
