---
description: 图像服务实现了一个简单的视觉水印工具。
seo-description: 图像服务实现了一个简单的视觉水印工具。
seo-title: 水印
solution: Experience Manager
title: 水印
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 水印{#watermarks}

图像服务实现了一个简单的视觉水印工具。

水印通常是半透明图像，但可能是文本或更复杂的分层复合图像。 在应用所有视图属性(、、、、)后，服务器将在回复图 `wid=`像上方 `hei=`放 `align=`置水 `scl=`印 `bgc=`层。

通过设置有效的目 `attribute::Watermark` 录条目（其中将包含水印图像或模板）来启用水印。 如果 `attribute::Watermark` 在指定的目录中设置，则服务器将向引用请求URL中的目录ID的所有图像请求添加水印。 如果 `default::Watermark` 设置了(在默认目录中 [!DNL default.ini])，则无论是否引用目录，水印都将应用于所有图像请求。

水印不会应用于响应缩略图请求( `req=tmb`)和Scene7查看器的某些请求而返回的图像。

## 缩放和对齐 {#section-89ef9e5926ae438abbd8e70332749b76}

指定水印后，服务器将首先生成需要应用水印的合成图像( *目标图像*)(在应用视图变换之前)。 然后，服务器为水印生成复合图像，就像任何其他图像(水印图 *像*)一样。

与标准图像不 `sizeN=` 同，可以为水印图像的layer=0或layer=comp指定。 这允许相对于目标图像缩放水印图像。 如果 `sizeN=` 未指定，则水印图像在与目标图像合并时保持其像素大小。

在水印记录中，请 `fmt=`求命令（如）和视图命令( `wid=`如)将被忽略，但除外 `align=`。 `align=` 可用于相对于水印图像相对于目标图像定位水印图像。 这允许水印相对于目标图像的角或边缘的定位。

缩放和对齐后，服务器将使用为水印图像或水印图像指定的和值在目标图 `blendMode=` 像 `opac=` 上方 `layer=0` 放置水印图 `layer=comp` 像层。 最后，应用为视图图像指定的请求和目标命令来构建回复图像。

请注意，水印图像永远不会扩展到通过和命令添加到回复图像的任何空白 `wid=` 空间 `hei=` 上。

## 示例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能由包含徽标或版权声明的简单RGBA图像组成。 我们会在图像目录（或默认目录）中创建一条设置为的记录， `catalog::Id` 并在 `watermark` 中指定水印图像文件 `catalog::Path`。 我们希望在保留少量额外边距的同时拉伸水印以适合视图图像（而不扭曲水印），并将不透明度降低到原始水印的20%，因此我们将其设 `catalog::Modifier` 置为 `sizeN=0.9,0.9&opac=20`。 要激活水印，请 `attribute::Watermark` 在此示例中将其设置为水印目录条目的id，即“watermark”。 我们可能希望尝试不同的选 `blendMode=` 择以获得不同的水印效果。

## 另请参阅 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[属性：:Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
