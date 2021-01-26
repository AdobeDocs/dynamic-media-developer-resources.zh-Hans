---
description: 变换应用于源图像和文本图层。
seo-description: 变换应用于源图像和文本图层。
seo-title: 图层变换
solution: Experience Manager
title: 图层变换
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 层变换{#layer-transforms}

变换应用于源图像和文本图层。

以下操作按给定顺序应用于源图像，以实现与第0层的所需空间关系：

1. 应用`crop=`（如果指定）。
1. 基于`size=`或者，如果未指定`size=`，则基于`scale=`；如果未指定`scale=`，则基于`res=`；如果未指定`res=`，则使用完整分辨率源图像。
1. 应用`flip=`（如果指定）。
1. 应用`rotate=`（如果指定）。
1. 应用`extend=`（如果指定）。
1. 根据`origin=`和`pos=`将图层放置到画布中（请参见下文）。

以下变换应用于文本图层：

1. 文本框大小由`size=`或文本宽度和高度决定，如果`size=`仅部分提供或根本不提供。 文本使用rtf文本对齐属性在文本框内对齐。 文本可能会被文本框裁剪。
1. 根据使用`textAttr=`指定的分辨率缩放文本内容。
1. 应用`rotate=`（如果指定）。
1. 应用`extend=`（如果指定）。
1. 根据`origin=`和`pos=`将图层放置到画布中（请参见下文）。

对于图像和文本图层，在画布中对图层进行最后一步定位不适用于图层0，因为图层0有效地构成了画布。
