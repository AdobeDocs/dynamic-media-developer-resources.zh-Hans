---
description: 图像集数据。 提供了一种机制，用于定义Dynamic Media查看器使用的已排序图像集和控制属性。
solution: Experience Manager
title: 图像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
TQID: 'https://experienceleague.adobe.com/wh25AlzBQv0W-lEugybS8B-cIYYFoK8o9I2uGb52Ui4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 681
ht-degree: 1%

---

# 图像集{#imageset}

图像集数据。 提供了一种机制，用于定义Dynamic Media查看器使用的已排序图像集和控制属性。

图像集由以逗号分隔的已排序项目列表组成。 每个项目由一个或多个子项目（图像ID、样本ID、媒体文件路径、标签等）组成，它们之间用分号或/和冒号隔开。

大括号`{ }`和括号`( )`可用于分隔某些内容（如颜色值）或指示嵌套集。 使用此方式的大括号或圆括号不能进行编码，必须始终显示为匹配对，否则会发生目录分析错误。

>[!NOTE]
>
>以下字符用作集分隔符，当这些字符作为id或字符串值的一部分显示在集中时，它们必须进行HTTP编码：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


有关图像集的结构和使用的其他详细信息，请参阅图像服务查看器文档。

服务器在响应`req=imageset`请求时不修改地返回此字段的内容。

## 标准集 {#section-5ecc8ffee7224668b63f601383665564}

图像服务本身支持以下集定义，对某些查看器的访问涉及服务器端解析、验证和处理集。 可以通过在`catalog::AssetType`中指定相应的值来标识每个集类型。

**基本样本集**

基本样本集中的每个项目均由对图像记录的引用和用作样本的图像记录的可选单独引用组成。

| `*`basicSwatchSet`*` | `*`样本项`*&#42;[',' *`样本项`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`样本`*]` |
| `*`样本`*` | `*`swatchId`*`\|`solidColorSpecifier` |
| `*`imageId`*` | IS图像引用（目录/ID） |
| `*`swatchId`*` | IS图像引用（目录/ID） |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`标签`*]'}'` |
| `*`rrggbb`*` | 用于纯色样本的打包6位十六进制RGB色值 |
| `*`标签`*` | 纯色样本的可选文本标签 |

**分层样本集**

分层样本集中的每个项目都可以由基本样本项目或样本集记录的引用组成（此类项目需要样本）。

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`*` \| `{` *`basicSwatchSetId`* &#39;；&#39; *`swatch`* `}` |
| `*`basicSwatchSetId`*` | 对定义基本样本集的目录记录的IS引用（目录/ID） |

**基本旋转集**

基本旋转集由图像ID的简单列表组成。

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**二维旋转集**

二维旋转集的每个项目都可以由简单图像、对基本旋转集的引用或由大括号分隔的线内基本旋转集组成。 可以使用圆括号代替大括号。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`*` \| `{` &#39;{&#39; *`basicSpinSet`* &#39;}&#39; `}` \| `*`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | 对定义基本旋转集的目录记录的IS引用（目录/ID） |

**页面集**

页面集中的每个项目最多可包含用冒号分隔的三页图像。

| `*`页面集`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**媒体集**

媒体集中的每个项目都可以由图像、基本样本集、分层样本集、基本旋转集、二维旋转集、页面集或视频资产组成。 每个媒体集项目也可以包含可选的色板和类型标识符。

| `*`媒体集`*` | `*`项`* &#42;[ , *`项`* ]` |
|---|---|
| `*`项`*` | `{ *`videoItem`*` \| *`recutItem`* \| *`imageItem`*`}}`\|*`setItem`*`}` `[` ； `[`*`ID`*`]` `[` ； `[`*`reserved`*`] ] ]` |
| `*`videoItem`*` | `*`视频`* ; *`色板ID`*` |
| `*`recutItem`*` | `*`recut`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | `{ *`setId`*` \| `{` &#39;{&#39; *`inlineSet`* &#39;}&#39; `} }` ； *`swatchId`* |
| `*`ID`*` | `media type identifier` `[` img \|基本\|高级图像\| img \| img \| img_set \|高级图像集\|高级样本集\|旋转\|视频`]` |
| `*`swatchId`*` | IS图像ID |
| `*`视频`*` | 视频/动画文件路径或静态目录ID |
| `*`剪辑`*` | 剪辑定义XML文件路径或静态目录ID |
| `*`imageId`*` | IS图像ID |
| `*`setId`*` | 对图像、旋转或ecatalog集的IS引用 |
| `*`inlineSet`*` | 内联图像、旋转或ecatalog集 |
| `*`保留`*` | 保留供将来使用 |

**Video Sets**

视频集由视频ID的简单列表组成，其中每个ID都引用静态内容目录中的一个条目。

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## 属性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文本字符串。 `catalog::Id`值、绝对图像服务器文件路径或相对于`attribute::RootPath`的文件路径的逗号分隔列表。 同一图像在集中可能会被多次引用。 定义目录记录可出现在集合的任何位置。

此字段参与文本字符串本地化。 除了&#x200B;*`label`*&#x200B;字符串（*`solidColorSpecifier`*&#x200B;的一部分）之外，如果所有分隔字段至少包含一个“`^loc=…^`”本地化令牌，则对其进行本地化。 有关详细信息，请参阅&#x200B;*HTTP协议引用*&#x200B;中的[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 默认 {#section-c3a60e360393478284f0f2d2da5b963b}

无。

## 請亦參閱 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ， [attribute：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)，[对象ID转换](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ，[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) ，图像服务查看器文档
