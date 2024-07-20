---
description: 响应req=tmb请求返回到客户端的图像是通过考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix从复合图像派生的。
solution: Experience Manager
title: 缩略图的视图转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# 缩略图的视图转换{#view-transform-for-thumbnails}

响应req=tmb请求返回到客户端的图像是通过考虑以下值从复合图像派生的：wid=、hei=、attribute：：DefaultThumbPix和attribute：：MaxPix。

1. **计算视图矩形** — 使用`wid=`或宽度值`attribute::DefaultThumbPix`作为视图矩形。 使用`hei=`或高度值`attribute::DefaultThumbPix`作为高度。 必须在此步骤中完全指定视图矩形。 （请注意，如果没有为图层0指定`size=`，则视图矩形与图层0矩形相同）。
1. **缩放复合** — 如果为`catalog::ThumbType=Crop`，则复合将缩放到尽可能小的图像，同时仍填充整个视图矩形；将裁剪额外的图像数据。 如果为`catalog::ThumbType= Fit`，则复合将缩放到尽可能大的图像，同时仍然将整个复合拟合到视图矩形。 如果`catalog::ThumbType=Texture`，则复合根本不进行缩放以保留`catalog::ThumbRes`中指定的分辨率。
1. **填充和裁切** — 视图矩形用`bgc=`颜色填充（如果未指定，则用`attribute::ThumbBkgColor`填充）。 使用属性： `ThumbHorizAlign`和属性： `ThumbVertAlign`将缩放的组合与视图矩形对齐。 缩放后的复合随即与填充视图矩形合并，而无需进一步缩放。 超出视图矩形的复合区域将被裁剪。
