---
description: 图像服务实现了简单的可视水印功能。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 水印{#watermarks}

图像服务实现了简单的可视水印功能。

水印通常为半透明图像，但也可能为文本，或更复杂的分层复合图像。 应用所有视图属性(`wid=`、`hei=`、`align=`、`scl=`、`bgc=`)后，服务器将水印叠加在回复图像上。

通过将`attribute::Watermark`设置为包含水印图像或模板的有效目录项来启用水印。 如果在指定目录中设置`attribute::Watermark`，则服务器会将水印添加到所有引用请求URL中的目录ID的图像请求。 如果设置`default::Watermark`（在默认目录[!DNL default.ini]中），则水印将应用于所有图像请求，无论它们是否引用目录。

水印不会应用于响应缩略图请求(`req=tmb`)以及Dynamic Media查看器的某些请求返回的图像。

## 缩放和对齐 {#section-89ef9e5926ae438abbd8e70332749b76}

指定水印时，服务器首先生成需要应用水印的复合图像（*目标图像*）（在应用视图转换之前）。 然后，服务器为水印生成复合图像，就像任何其他图像（*水印图像*）一样。

与标准图像不同，可以为水印图像的layer=0或layer=comp指定`sizeN=`。 这允许相对于目标图像缩放水印图像。 如果未指定`sizeN=`，则水印图像在与目标图像合并时保留其像素大小。

请求命令（如`fmt=`）和视图命令（如`wid=`）在水印记录中被忽略，但`align=`除外。 `align=`可用于相对于水印图像相对于目标图像定位水印图像。 这允许相对于目标图像的角或边缘定位水印。

缩放和对齐后，服务器使用为水印图像的`blendMode=`或`opac=`指定的`layer=0`和`layer=comp`值在目标图像上叠加水印图像。 最后，应用为目标图像指定的请求和视图命令来构造回复图像。

请注意，水印图像决不会超过`wid=`和`hei=`命令添加到回复图像的任何空格。

## 示例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能包含包含包含徽标或版权声明的简单RGBA图像。 我们在图像目录（或默认目录）中创建记录（将`catalog::Id`设置为`watermark`），并在`catalog::Path`中指定水印图像文件。 我们希望拉伸水印以适合视图图像（不扭曲水印），同时保留一些额外的边距，并将不透明度降低到原始水印的20%，因此我们将`catalog::Modifier`设置为`sizeN=0.9,0.9&opac=20`。 要激活水印，请将`attribute::Watermark`设置为水印目录项的ID，在本例中为“水印”。 我们可能会尝试使用不同的`blendMode=`选项来实现不同的水印效果。

## 另请参阅 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute：：水印](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
