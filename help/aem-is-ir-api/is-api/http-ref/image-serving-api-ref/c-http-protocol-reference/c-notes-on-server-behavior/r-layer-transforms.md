---
description: 转换将应用于源图像和文本图层。
solution: Experience Manager
title: 图层转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
TQID: 'https://experienceleague.adobe.com/jChFcZzWWOlbicpu0WeRSJb608dGT9JmVSItV-uEjBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# 图层转换{#layer-transforms}

转换将应用于源图像和文本图层。

对源图像按照给定的顺序进行如下操作，以获得与第0层的期望空间关系：

1. 应用`crop=`（如果已指定）。
1. 基于`size=`进行缩放；如果未指定`size=`，则基于`scale=`；如果未指定`scale=`，则基于`res=`；如果未指定`res=`，则使用全分辨率源图像。
1. 应用`flip=`（如果已指定）。
1. 应用`rotate=`（如果已指定）。
1. 应用`extend=`（如果已指定）。
1. 根据`origin=`和`pos=`在画布中放置图层（见下文）。

以下转换将应用于文本图层：

1. 文本框大小由`size=`决定，或者由文本宽度和高度决定（如果`size=`仅部分提供或完全未提供）。 使用rtf文本对齐属性，在文本框中对齐文本。 文本可能被文本框裁剪。
1. 根据用`textAttr=`指定的分辨率缩放文本内容。
1. 应用`rotate=`（如果已指定）。
1. 应用`extend=`（如果已指定）。
1. 根据`origin=`和`pos=`将图层放置在画布中（见下文）。

对于图像和文本图层，在画布中最后一步定位图层不适用于图层0，因为图层0有效地构成了画布。
