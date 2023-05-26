---
description: 转换将应用于源图像和文本图层。
solution: Experience Manager
title: 图层转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# 图层转换{#layer-transforms}

转换将应用于源图像和文本图层。

对源图像按照给定的顺序进行以下操作，以获得与第0层的期望空间关系：

1. 应用 `crop=`，如果指定。
1. 缩放依据 `size=` 或，如果 `size=` 未指定，基于 `scale=`，或者，如果 `scale=` 未指定，基于 `res=`，或者，如果 `res=`未指定，请使用完全分辨率的源图像。
1. 应用 `flip=`，如果指定。
1. 应用 `rotate=`，如果指定。
1. 应用 `extend=`，如果指定。
1. 根据以下内容将图层放置在画布中 `origin=` 和 `pos=` （见下文）。

以下转换将应用于文本图层：

1. 文本框的大小由以下因素决定 `size=`或文本宽度和高度，如果 `size=` 仅部分提供或根本不提供。 使用rtf文本对齐属性，文本在文本框中对齐。 文本可能被文本框裁剪。
1. 根据指定的分辨率缩放文本内容 `textAttr=`.
1. 应用 `rotate=`，如果指定。
1. 应用 `extend=`，如果指定。
1. 根据以下内容将图层放置在画布中 `origin=` 和 `pos=`（见下文）。

对于图像和文本图层，在画布中定位图层的最后一步不适用于图层0，因为图层0有效地构成了画布。
