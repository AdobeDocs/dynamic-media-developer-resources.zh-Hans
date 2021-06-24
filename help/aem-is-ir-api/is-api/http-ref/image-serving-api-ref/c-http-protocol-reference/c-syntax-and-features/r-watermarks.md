---
description: 图像服务实现了一个简单的视觉水印工具。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 1%

---

# 水印{#watermarks}

图像服务实现了一个简单的视觉水印工具。

水印通常是半透明图像，但可能是文本，或者是更复杂的分层复合图像。 在应用所有视图属性(`wid=`、`hei=`、`align=`、`scl=`、`bgc=`)后，服务器将在回复图像上层层水印。

通过将`attribute::Watermark`设置为包含水印图像或模板的有效目录条目，可启用水印。 如果在命名目录中设置`attribute::Watermark`，则服务器将向所有引用请求URL中目录ID的图像请求添加水印。 如果设置了`default::Watermark`（在默认目录中，[!DNL default.ini]），则水印将应用于所有图像请求，而不管它们是否引用了目录。

水印不会应用于响应缩略图请求(`req=tmb`)和Dynamic Media查看器的某些请求而返回的图像。

## 缩放和对齐 {#section-89ef9e5926ae438abbd8e70332749b76}

当指定水印时，服务器将首先生成需要应用水印的复合图像（*目标图像*）（在应用视图转换之前）。 然后，服务器为水印生成复合图像，就像任何其他图像（*水印图像*）一样。

与标准图像不同，`sizeN=`可以为水印图像的layer=0或layer=comp指定。 这允许相对于目标图像缩放水印图像。 如果未指定`sizeN=`，则水印图像在与目标图像合并时保持其像素大小。

在水印记录中，请求命令（如`fmt=`）和视图命令（如`wid=`）将被忽略，但`align=`除外。 `align=` 可用于相对于水印图像相对于目标图像定位水印图像。这允许水印相对于目标图像的角或边缘的定位。

在缩放和对齐后，服务器将使用为水印图像的`layer=0`或`layer=comp`指定的`blendMode=`和`opac=`值在目标图像上层叠水印图像。 最后，应用为目标图像指定的请求和视图命令来构建返回图像。

请注意，水印图像永远不会通过`wid=`和`hei=`命令扩展到返回图像中添加的任何空白空间。

## 示例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能由包含徽标或版权声明的简单RGBA图像组成。 我们在将`catalog::Id`设置为`watermark`的图像目录（或默认目录）中创建记录，并在`catalog::Path`中指定水印图像文件。 我们希望将水印拉伸到适合视图图像（不扭曲水印）的同时保留一点额外的边距，并将不透明度降低到原始水印的20%，因此我们将`catalog::Modifier`设置为`sizeN=0.9,0.9&opac=20`。 要激活水印，请将`attribute::Watermark`设置为水印目录条目的ID，此示例中的“水印”。 我们可能想尝试使用不同的`blendMode=`选项来实现不同的水印效果。

## 另请参阅 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[属性：:Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
