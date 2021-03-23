---
description: 变换应用于源图像和文本图层。
seo-description: 变换应用于源图像和文本图层。
seo-title: 图层变换
solution: Experience Manager
title: 图层变换
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# 图层变换{#layer-transforms}

变换应用于源图像和文本图层。

以下操作按给定顺序应用于源图像，以实现与图层0的所需空间关系：

1. 如果指定，请应用`crop=`。
1. 基于`size=`或者，如果未指定`size=`，则基于`scale=`；如果未指定`scale=`，则基于`res=`，或者，如果未指定`res=`，则使用全分辨率源图像。
1. 如果指定，请应用`flip=`。
1. 如果指定，请应用`rotate=`。
1. 如果指定，请应用`extend=`。
1. 根据`origin=`和`pos=`将图层放置在画布中（见下文）。

以下变换应用于文本图层：

1. 文本框大小由`size=`或文本宽度和高度决定，如果`size=`仅部分提供或根本不提供。 文本使用rtf文本对齐属性在文本框中对齐。 文本可能会被文本框裁剪。
1. 根据使用`textAttr=`指定的分辨率缩放文本内容。
1. 如果指定，请应用`rotate=`。
1. 如果指定，请应用`extend=`。
1. 根据`origin=`和`pos=`在画布中放置图层（见下面）。

对于图像图层和文本图层，在画布中定位图层的最后一步不会应用于图层0，因为图层0有效地构成了画布。
