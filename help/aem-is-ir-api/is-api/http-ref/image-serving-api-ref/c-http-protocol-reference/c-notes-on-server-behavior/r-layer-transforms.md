---
description: 变换应用于源图像和文本图层。
seo-description: 变换应用于源图像和文本图层。
seo-title: 图层变换
solution: Experience Manager
title: 图层变换
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图层变换{#layer-transforms}

变换应用于源图像和文本图层。

以下操作按给定顺序应用于源图像，以实现与图层0的所需空间关系：

1. 如果 `crop=`指定，则应用。
1. 根据或( `size=` 如果未指 `size=` 定)、基于或（如果未指定）、基于或（如果未指定）、基于或（如果未指定），使用全分 `scale=``scale=``res=``res=`辨率源图像（如果未指定）进行缩放。
1. 如果 `flip=`指定，则应用。
1. 如果 `rotate=`指定，则应用。
1. 如果 `extend=`指定，则应用。
1. 根据和（请参阅下面）将图 `origin=` 层放 `pos=` 置在画布中。

以下变换应用于文本图层：

1. 文本框大小由文本宽 `size=`度和高度决定(如果只提供部 `size=` 分或根本不提供)。 文本使用rtf文本对齐属性在文本框内对齐。 文本可能会被文本框裁剪。
1. 根据指定的分辨率缩放文本内容 `textAttr=`。
1. 如果 `rotate=`指定，则应用。
1. 如果 `extend=`指定，则应用。
1. 根据和（请参阅下面）将图 `origin=` 层放 `pos=`置在画布中。

对于图像图层和文本图层，在画布中对图层进行最后一步定位的操作不适用于图层0，因为图层0有效地构成了画布。
