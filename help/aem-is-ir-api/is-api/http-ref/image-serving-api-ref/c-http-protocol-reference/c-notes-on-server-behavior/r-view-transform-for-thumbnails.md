---
description: 响应req=tmb请求返回给客户端的图像是从复合图像派生的，方法是考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix。
seo-description: 响应req=tmb请求返回给客户端的图像是从复合图像派生的，方法是考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix。
seo-title: 视图变换缩览图
solution: Experience Manager
title: 视图变换缩览图
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 视图缩览图转换{#view-transform-for-thumbnails}

响应req=tmb请求返回给客户端的图像是从复合图像中派生的，方法是考虑以下值：wid=、hei=、attribute::DefaultThumbPix和attribute::MaxPix。

1. **计算视图矩** 形- `wid=` 使用视图矩 `attribute::DefaultThumbPix` 形的宽度或宽度值。使用`hei=`或高度值`attribute::DefaultThumbPix`作为高度。 必须在此步骤中完全指定视图矩形。 (请注意，如果没有为层0指定`size=`,视图矩形将与层0矩形相同)。
1. **缩放复合图像** -如果 `catalog::ThumbType=Crop`仍填充整个视图矩，则将复合图像缩放为尽可能小的图像；额外的图像数据被裁掉。如果`catalog::ThumbType= Fit`，则合成将缩放到可能的最大图像，同时仍将整个合成适合到视图矩形中。 如果`catalog::ThumbType=Texture`，则不会缩放合成以保留在`catalog::ThumbRes`中指定的分辨率。
1. **填充和裁剪** -视图矩形填充 `bgc=` 了颜色(如果未指定，则使用 `attribute::ThumbBkgColor`)。缩放复合图像使用以下属性与视图矩形对齐：`ThumbHorizAlign`和属性：`ThumbVertAlign`。 然后，缩放复合物与填充的视图矩形合并，而无需进一步缩放。 超出视图矩形的合成的任何区域都会被裁掉。

