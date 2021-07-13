---
description: 图像集数据。 提供了一种机制来定义排序的图像集和Dynamic Media查看器使用的控制属性。
solution: Experience Manager
title: 图像集
feature: Dynamic Media Classic，SDK/API，图像集
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 2%

---

# 图像集{#imageset}

图像集数据。 提供了一种机制来定义排序的图像集和Dynamic Media查看器使用的控制属性。

图像集由以逗号分隔的已排序项目列表组成，每个项目由一个或多个子项目（图像id、样本id、媒体文件路径、标签等）组成，并由分号和/或冒号分隔。

大括号`{ }`和圆括号`( )`可用于分隔某些内容（如颜色值）或指示嵌套集。 以这种方式使用的大括号或圆括号不得进行编码，且必须始终显示为匹配对，否则将发生目录解析错误。

>[!NOTE]
>
>以下字符用作设置的分隔符，且当它们作为id或字符串值的一部分显示在集中时，必须采用HTTP编码：
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



有关图像集的结构和用法的更多详细信息，请参阅图像服务查看器文档。

服务器会返回此字段的内容，而无需修改，以响应`req=imageset`请求。

## 标准集 {#section-5ecc8ffee7224668b63f601383665564}

图像服务本地支持以下集定义，通过某些查看器访问涉及对集进行服务器端解析、验证和处理。 可通过在`catalog::AssetType`中指定相应的值来标识每个集类型。

**基本色板集**

基本样本集中的每个项目都包含对图像记录的引用和对用作样本的图像记录的可选单独引用。

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIdswatch`*]` |
| `*`色板`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | IS图像引用（目录/id） |
| `*`swatchId`*` | IS图像引用（目录/id） |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rrggbblabel`*]'}'` |
| `*`rggbb`*` | 为实色色板打包了6位十六进制RGB颜色值 |
| `*`label`*` | 纯色色板的可选文本标签 |

**分层样本集**

分层样本集中的每个项目都可以包含基本样本项目或对样本集记录的引用（此类项目需要样本）。

| `*`hierarchicalSwatchSet`*` | `*``* &#42;[ ',' *`hierarchicalSwatchItemhierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | 对定义基本色板集的目录记录的IS引用（目录/ID） |

**基本旋转集**

基本旋转集由简单的图像ID列表组成。

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**二维旋转集**

二维旋转集中的每个项目都可以包含一个简单的图像、对基本旋转集的引用，或者一个以大括号分隔的内嵌基本旋转集。 可以使用圆括号而不是大括号。

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | 对定义基本旋转集的目录记录的IS引用（目录/ID） |

**页面集**

页面集中的每个项目最多可以包含三个使用冒号分隔的页面图像。

| `*`pageSet`*` | `*``* &#42;[ , *`pageItempageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageImageId`* ] ]` |

**媒体集**

媒体集中的每个项目都可以包含图像、基本色板集、分层色板集、基本旋转集、二维旋转集、页面集或视频资产。 每个媒体集项目还可以包含可选样本和类型标识符。

| `*`mediaSet`*` | `*``* &#42;[ , *`itemitem`* ]` |
|---|---|
| `*`项目`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videowatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | IS图像ID |
| `*`视频`*` | 视频/动画文件路径或静态目录ID |
| `*`重排`*` | 重定向定义XML文件路径或静态目录ID |
| `*`imageId`*` | IS图像ID |
| `*`setId`*` | 对图像、旋转或ecatalog集的引用 |
| `*`inlineSet`*` | 内嵌的图像、旋转或ecatalog集 |
| `*`已保留`*` | 保留供将来使用 |

**Video Sets**

视频集由视频ID的简单列表组成，其中每个ID都引用静态内容目录中的一个条目。

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## 属性 {#section-17c731e5c46646aa90ac21f39bb693ca}

文本字符串。 以逗号分隔的`catalog::Id`值列表、绝对图像服务器文件路径或相对于`attribute::RootPath`的文件路径。 同一图像在集中可能被引用多次。 定义目录记录可能显示在任意位置的集合中。

此字段参与文本字符串本地化。 除了&#x200B;*`label`*&#x200B;字符串（*`solidColorSpecifier`*&#x200B;的一部分）之外，如果所有分隔字段至少包含一个“ `^loc=…^`”本地化令牌，则这些字段都会进行本地化。 有关详细信息，请参阅&#x200B;*HTTP协议引用*&#x200B;中的[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

## 默认 {#section-c3a60e360393478284f0f2d2da5b963b}

无。

## 另请参阅 {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md),  [对象ID转换](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ,  [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Image Serving Viewers文档
