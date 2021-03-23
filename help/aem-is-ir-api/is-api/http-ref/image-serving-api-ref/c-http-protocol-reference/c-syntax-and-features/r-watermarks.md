---
description: 图像服务实现了一个简单的视觉水印工具。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 1%

---


# 水印{#watermarks}

图像服务实现了一个简单的视觉水印工具。

水印通常是半透明图像，但可能是文本或更复杂的分层复合图像。 在应用所有视图属性(`wid=`、`hei=`、`align=`、`scl=`、`bgc=`)后，服务器将在回复图像上层覆盖水印。

通过将`attribute::Watermark`设置为包含水印图像或模板的有效目录条目来启用水印。 如果`attribute::Watermark`在命名目录中设置，服务器将向引用请求URL中目录id的所有图像请求添加水印。 如果设置了`default::Watermark`（在默认目录中，[!DNL default.ini]），则无论水印是否引用了目录，都将应用于所有图像请求。

水印不会应用于响应缩略图请求(`req=tmb`)和来自Dynamic Media查看器的某些请求而返回的图像。

## 缩放和对齐{#section-89ef9e5926ae438abbd8e70332749b76}

指定水印后，服务器将首先生成需要应用水印的合成图像(*目标图像*)(在应用视图变换之前)。 然后，服务器为水印生成复合图像，就像任何其他图像一样（*水印图像*）。

与标准图像不同，可以为水印图像的layer=0或layer=comp指定`sizeN=`。 这允许相对于目标图像缩放水印图像。 如果未指定`sizeN=`，则当与目标图像合并时，水印图像将保持其像素大小。

在水印记录中，请求命令（如`fmt=`）和视图命令（如`wid=`）将被忽略，但`align=`除外。 `align=` 可用于相对于水印图像相对于目标图像定位水印图像。这允许水印相对于目标图像的角或边缘的定位。

缩放和对齐后，服务器将使用为水印图像的`layer=0`或`layer=comp`指定的`blendMode=`和`opac=`值将水印图像层叠在目标图像上。 最后，应用为目标图像指定的请求和视图命令来构造回复图像。

请注意，水印图像永远不会扩展到通过`wid=`和`hei=`命令添加到回复图像的任何空白。

## 示例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能由包含徽标或版权声明的简单RGBA图像组成。 我们在图像目录（或默认目录）中创建一条将`catalog::Id`设置为`watermark`的记录，并在`catalog::Path`中指定水印图像文件。 我们希望在保留少量额外边距的同时拉伸水印以适合视图图像（不扭曲水印），并将不透明度降低到原始水印的20%，因此我们将`catalog::Modifier`设置为`sizeN=0.9,0.9&opac=20`。 要激活水印，请将`attribute::Watermark`设置为此示例中水印目录条目“watermark”的id。 我们可能希望尝试不同的`blendMode=`选项，以获得不同的水印效果。

## 另请参阅 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[属性：:Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
