---
description: 响应req=tmb请求返回到客户端的图像是通过考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix从复合图像派生的。
solution: Experience Manager
title: 缩略图的视图转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 缩略图的视图转换{#view-transform-for-thumbnails}

响应req=tmb请求返回到客户端的图像是通过考虑以下值从复合图像派生的： wid=、hei=、attribute：：DefaultThumbPix和attribute：：MaxPix。

1. **计算视图矩形**  — 使用 `wid=` 或宽度值 `attribute::DefaultThumbPix` 作为视图矩形的宽度。 使用 `hei=` 或高度值 `attribute::DefaultThumbPix` 对于高度。 必须在此步骤中完全指定视图矩形。 (请注意，视图矩形与图层0矩形相同（如果没有） `size=`指定给层0)。
1. **缩放复合** - If `catalog::ThumbType=Crop`，则复合图像会被缩放到尽可能小的图像，同时仍会填充整个视图；额外的图像数据会被裁剪。 如果 `catalog::ThumbType= Fit`，则复合图像会缩放到尽可能大的图像，同时仍会将整个复合图像拟合到视图矩中。 如果 `catalog::ThumbType=Texture`，则复合根本不进行缩放以保留中指定的分辨率 `catalog::ThumbRes`.
1. **填充和裁切**  — 视图矩形填充 `bgc=` 颜色(如果未指定，则使用 `attribute::ThumbBkgColor`)。 缩放的复合使用属性与视图矩形对齐： `ThumbHorizAlign` 和属性： `ThumbVertAlign`. 缩放的复合随即会与填充视图矩形合并，而无需进一步缩放。 超出视图矩形的复合区域将被裁剪。
