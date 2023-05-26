---
description: 图像服务实现了一个简单的可视水印功能。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# 水印{#watermarks}

图像服务实现了一个简单的可视水印功能。

水印通常为半透明图像，但也可能为文本或更复杂、分层的复合图像。 服务器将在所有视图属性( `wid=`， `hei=`， `align=`， `scl=`， `bgc=`)已应用。

可通过设置启用水印 `attribute::Watermark` 到包含水印图像或模板的有效目录条目。 如果 `attribute::Watermark` 在命名目录中设置，则服务器会将水印添加到所有引用请求URL中的目录ID的图像请求。 如果 `default::Watermark` 设置(在默认目录中， [!DNL default.ini])，水印将应用于所有图像请求，无论它们是否引用目录。

水印不会应用于响应缩略图请求返回的图像( `req=tmb`)，以及来自Dynamic Media查看者的某些请求。

## 缩放和对齐 {#section-89ef9e5926ae438abbd8e70332749b76}

指定水印后，服务器将首先生成复合图像(即 *目标图像*)中需要应用水印（在应用视图转换之前）。 然后，服务器为水印生成复合图像，就像任何其他图像一样( *水印图像*)。

与标准图像不同， `sizeN=` 可以为水印图像的layer=0或layer=comp指定。 这允许水印图像相对于目标图像进行缩放。 如果 `sizeN=` 如果未指定，则水印图像在与目标图像合并时保留其像素大小。

请求命令(例如 `fmt=`)和view命令(例如 `wid=`)在水印记录中被忽略，但以下情况除外 `align=`. `align=` 可用于相对于水印图像相对于目标图像定位水印图像。 这允许相对于目标图像的角或边缘定位水印。

缩放和对齐后，服务器将使用将水印图像叠加到目标图像上 `blendMode=` 和 `opac=` 指定的值 `layer=0` 或 `layer=comp` 水印图像的。 最后，使用为目标图像指定的请求和视图命令来构造回复图像。

请注意，水印图像绝不会超过由向回复图像添加的任何空格 `wid=` 和 `hei=` 命令。

## 示例 {#section-0408c977d7324d4cb0e76a91cdfa2acd}

典型的水印可能包含包含包含徽标或版权声明的简单RGBA图像。 我们使用在图像目录（或默认目录）中创建记录 `catalog::Id` 设置为 `watermark` 并在中指定水印图像文件 `catalog::Path`. 在保留少量额外边界的同时，对水印进行拉伸以符合视图图像（水印不失真），并将水印的不透明度降低到原始水印的20%，因此我们设置 `catalog::Modifier` 到 `sizeN=0.9,0.9&opac=20`. 要激活水印，请设置 `attribute::Watermark` 至水印目录条目的id，在本例中为“水印”。 我们可能会想用不同的 `blendMode=` 选择实现不同的水印效果。

## 另请参阅 {#section-4d66713abacb42c7b6a0c93cbf966a97}

[属性：：水印](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
