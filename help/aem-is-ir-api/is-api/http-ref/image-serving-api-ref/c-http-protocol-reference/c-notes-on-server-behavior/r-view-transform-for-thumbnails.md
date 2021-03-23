---
description: 响应req=tmb请求返回给客户的图像是从复合图像派生的，方法是考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix。
seo-description: 响应req=tmb请求返回给客户的图像是从复合图像派生的，方法是考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix。
seo-title: 视图变换缩览图
solution: Experience Manager
title: 视图变换缩览图
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---


# 缩览图的视图变换{#view-transform-for-thumbnails}

响应req=tmb请求返回给客户端的图像是从复合图像派生的，方法是考虑以下值：wid=、hei=、attribute::DefaultThumbPix和attribute::MaxPix。

1. **计算视图矩形**  — 使 `wid=` 用视图矩 `attribute::DefaultThumbPix` 形的宽度或宽度值。使用`hei=`或`attribute::DefaultThumbPix`的高度值作为高度。 必须在此步骤中完全指定视图矩形。 (请注意，如果没有为图层0指定`size=`，则视图矩形将与图层0矩形相同)。
1. **缩放合成**  — 如果 `catalog::ThumbType=Crop`，则在仍填充整个视图矩形的同时，将合成缩放为尽可能小的图像；额外的图像数据会被裁掉。如果`catalog::ThumbType= Fit`，则合成将缩放到最大图像，同时仍将整个合成拟合到视图矩形中。 如果`catalog::ThumbType=Texture`，则不缩放合成以保留在`catalog::ThumbRes`中指定的分辨率。
1. **填充和裁剪** -视图矩形用颜色 `bgc=` 填充(如果未指定，则用 `attribute::ThumbBkgColor`)。缩放复合图像使用以下属性与视图矩形对齐：`ThumbHorizAlign`和属性：`ThumbVertAlign`。 然后，缩放的合成与填充的视图矩形合并，而不进一步缩放。 超出视图矩形的任何复合区域都会被裁掉。

