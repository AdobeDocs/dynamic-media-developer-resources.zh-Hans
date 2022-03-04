---
description: 图像服务实现了一个简单的视觉水印工具。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# 水印{#watermarks}

图像服务实现了一个简单的视觉水印工具。

水印通常是半透明图像，但可能是文本，或者是更复杂的分层复合图像。 服务器将在所有视图属性( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`)。

通过设置 `attribute::Watermark` 到包含水印图像或模板的有效目录条目。 如果 `attribute::Watermark` 在命名目录中设置，则服务器会将水印添加到所有引用请求URL中目录id的图像请求中。 如果 `default::Watermark` 设置(在默认目录中， [!DNL default.ini])，则无论水印是否引用目录，都会将其应用于所有图像请求。

水印不会应用于响应缩略图请求而返回的图像( `req=tmb`)和Dynamic Media查看器的某些请求。

## 缩放和对齐 {#section-89ef9e5926ae438abbd8e70332749b76}

当指定水印时，服务器将首先生成复合图像( *目标图像*)，在应用视图转换之前，需要将水印应用到该位置。 然后，服务器会像任何其他图像( *水印图像*)。

与标准图像不同， `sizeN=` 可以为水印图像的layer=0或layer=comp指定。 这允许相对于目标图像缩放水印图像。 如果 `sizeN=` 未指定，水印图像在与目标图像合并时保持其像素大小。

请求命令(例如 `fmt=`)和查看命令(例如 `wid=`)会在水印记录中忽略，但 `align=`. `align=` 可用于相对于水印图像相对于目标图像定位水印图像。 这允许水印相对于目标图像的角或边缘的定位。

缩放和对齐后，服务器将使用 `blendMode=` 和 `opac=` 为 `layer=0` 或 `layer=comp` 水印图像。 最后，应用为目标图像指定的请求和视图命令来构建返回图像。

请注意，水印图像永远不会扩展到 `wid=` 和 `hei=` 中。

## 示例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能由包含徽标或版权声明的简单RGBA图像组成。 我们在图像目录（或默认目录）中使用 `catalog::Id` 设置为 `watermark` 并在中指定水印图像文件 `catalog::Path`. 我们希望在保留少量额外边距的同时，将水印拉伸以适合视图图像（不扭曲水印），并将不透明度降低到原始水印的20%，因此我们设置 `catalog::Modifier` to `sizeN=0.9,0.9&opac=20`. 要激活水印，请设置 `attribute::Watermark` 到水印目录条目的id，此示例中的“水印”。 我们可能想用不同的 `blendMode=` 实现不同水印效果的选项。

## 另请参阅 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[属性：:Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
