---
description: 图像集数据。 提供一种机制，用于定义已排序的图像集并控制Dynamic Media查看器使用的属性。
solution: Experience Manager
title: 图像集
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---


# 图像集{#imageset}

图像集数据。 提供一种机制，用于定义已排序的图像集并控制Dynamic Media查看器使用的属性。

图像集由按逗号分隔的按排序项列表组成，每个项由一个或多个子项（图像id、样本id、媒体文件路径、标签等）组成，由分号和/或冒号分隔。

大括号`{ }`和圆括号`( )`可用于分隔某些内容（如颜色值）或指示嵌套集。 以这种方式使用的大括号或小括号不能进行编码，并且必须始终显示为匹配对，否则将发生目录分析错误。

>[!NOTE]
>
>以下字符用作集分隔符，当它们作为id或字符串值的一部分出现在集中时，必须进行HTTP编码：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



有关图像集结构和使用的其他详细信息，请参阅图像服务查看器文档。

服务器返回此字段的内容，而无需修改以响应`req=imageset`请求。

## 标准集{#section-5ecc8ffee7224668b63f601383665564}

图像服务本身支持以下集定义，通过某些查看器访问涉及对集的服务器端分析、验证和处理。 通过在`catalog::AssetType`中指定相应值，可以标识每个集类型。

**基本色板集**

基本样本集中的每个项目都包含对图像记录的引用和对用作样本的图像记录的可选单独引用。

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageIdswatch`*[';' *``*]` |
| `*`色板`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS图像引用（目录/id） |
| `*`swatchId`*` | IS图像引用（目录/id） |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rrggbblabel`*]'}'` |
| `*`rggbb`*` | 为纯色色板打包了6位十六进制RGB颜色值 |
| `*`label`*` | 纯色色板的可选文本标签 |

**分层色板集**

分层样本集中的每个项目都可以包含基本样本项目或对样本集记录的引用（此类项目需要样本）。

| `*`hierarchicalSwatchSet`*` | `*``* &#42;[ ',' *`hierarchicalSwatchItemhierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | IS引用(catalog/id)到定义基本色板集的目录记录 |

**基本旋转集**

基本旋转集由图像ID的简单列表组成。

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**二维旋转集**

二维旋转集中的每个项目都可以由简单图像、对基本旋转集的引用或由花括号分隔的内联基本旋转集组成。 可以使用圆括号代替花括号。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | 对定义基本旋转集的目录记录的IS引用(catalog/id) |

**页面集**

页面集中的每个项目最多可包含三个用冒号分隔的页面图像。

| `*`pageSet`*` | `*``* &#42;[ , *`pageItempageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageImageIdimageId`* ] ]` |

**媒体集**

媒体集中的每个项目都可以包含图像、基本样本集、分层样本集、基本旋转集、二维旋转集、页面集或视频资产。 每个媒体集项目还可包含可选色板和类型标识符。

| `*`mediaSet`*` | `*``* &#42;[ , *`itemitem`* ]` |
|---|---|
| `*`项目`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS图像ID |
| `*`视频`*` | 视频/动画文件路径或静态目录ID |
| `*`重`*` | 剪辑定义XML文件路径或静态目录ID |
| `*`imageId`*` | IS图像ID |
| `*`setId`*` | 对图像、旋转或对话集的IS引用 |
| `*`inlineSet`*` | 内嵌的图像、旋转或电子目录集 |
| `*`已保留`*` | 保留供将来使用 |

**Video Sets**

视频集由视频ID的简单列表组成，其中每个ID引用静态内容目录中的一个条目。

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## 属性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文本字符串。 以逗号分隔的`catalog::Id`值、绝对图像服务器文件路径或相对于`attribute::RootPath`的文件路径的列表。 同一图像在集合中可以多次被引用。 定义目录记录可能出现在集中的任意位置。

此字段参与文本字符串本地化。 除了&#x200B;*`label`*&#x200B;字符串（*`solidColorSpecifier`*&#x200B;的一部分）之外，如果所有分隔字段至少包含一个“ `^loc=…^`”本地化令牌，则这些字段将本地化。 有关详细信息，请参阅&#x200B;*HTTP协议参考*&#x200B;中的[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 默认 {#section-c3a60e360393478284f0f2d2da5b963b}

无。

## 另请参阅 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ，属 [性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)，对象 [ID转换，文本字](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) 符串本地化 [](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) ，图像服务查看器文档
