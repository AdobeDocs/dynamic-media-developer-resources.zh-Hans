---
description: 响应req=tmb请求返回给客户端的图像，通过考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix从复合图像派生。
solution: Experience Manager
title: 查看缩览图转换
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 查看缩览图转换{#view-transform-for-thumbnails}

响应req=tmb请求返回给客户端的图像通过考虑以下值从复合图像派生：wid=、hei=、attribute::DefaultThumbPix和attribute::MaxPix。

1. **计算视图矩形**  — 对 `wid=` 于视图矩形 `attribute::DefaultThumbPix` 的宽度，使用或的宽度值。使用`hei=`或高度值`attribute::DefaultThumbPix`表示高度。 必须在此步骤中完全指定视图直接。 （请注意，如果没有为层0指定`size=`，则视图直接将与层0直接相同）。
1. **缩放复合图像**  — 如果 `catalog::ThumbType=Crop`，则在仍填充整个视图的同时，将复合图像缩放为尽可能小的图像；额外的图像数据会被裁剪掉。如果`catalog::ThumbType= Fit`，则复合图像会缩放到最大图像，同时仍将整个复合图像拟合到视图矩形中。 如果`catalog::ThumbType=Texture`，则根本不会缩放复合图以保留`catalog::ThumbRes`中指定的分辨率。
1. **填充和裁剪**  — 视图矩形中填充了 `bgc=` 颜色(或者，如果未指定，使用 `attribute::ThumbBkgColor`)。缩放的复合图像使用属性与视图方向对齐：`ThumbHorizAlign`和属性：`ThumbVertAlign`。 然后，缩放的复合图与填充视图矩形合并，而无需进一步缩放。 超出视图矩形范围的复合的任何区域都会被裁剪掉。
