---
description: 转换应用于源图像和文本层。
solution: Experience Manager
title: 图层转换
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 图层转换{#layer-transforms}

转换应用于源图像和文本层。

以下操作按给定顺序应用于源图像，以与层0达到所需的空间关系：

1. 如果指定，则应用`crop=`。
1. 根据`size=`或未指定`size=`、基于`scale=`或未指定`scale=`、基于`res=`或未指定`res=`的缩放，使用全分辨率源图像。
1. 如果指定，则应用`flip=`。
1. 如果指定，则应用`rotate=`。
1. 如果指定，则应用`extend=`。
1. 根据`origin=`和`pos=`在画布中放置图层（请参阅下文）。

以下转换将应用于文本层：

1. 文本框大小由`size=`决定，或者如果`size=`仅部分提供或根本不提供，则文本宽度和高度决定。 文本使用rtf文本对齐属性在文本框内对齐。 文本可能会被文本框裁剪。
1. 根据使用`textAttr=`指定的分辨率缩放文本内容。
1. 如果指定，则应用`rotate=`。
1. 如果指定，则应用`extend=`。
1. 在画布中根据`origin=`和`pos=`放置图层（请参阅下文）。

对于图像层和文本层，在画布中定位图层的最后一步不会应用到图层0，因为图层0有效地构成了画布。
