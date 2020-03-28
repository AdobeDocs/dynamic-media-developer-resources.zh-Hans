---
description: 响应req=tmb请求返回给客户端的图像是从复合图像派生的，方法是考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix。
seo-description: 响应req=tmb请求返回给客户端的图像是从复合图像派生的，方法是考虑以下值wid=、hei=、属性DefaultThumbPix和属性MaxPix。
seo-title: 视图缩览图变换
solution: Experience Manager
title: 视图缩览图变换
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# 视图缩览图变换{#view-transform-for-thumbnails}

响应于req=tmb请求返回给客户端的图像通过考虑以下值从合成图像派生：wid=、hei=、attribute::DefaultThumbPix和attribute::MaxPix。

1. **计算视图矩形** -使 `wid=` 用矩形的宽度值 `attribute::DefaultThumbPix` 或视图矩形的宽度值。 请 `hei=` 使用或高度 `attribute::DefaultThumbPix` 值作为高度。 必须在此步骤中完全指定视图矩形。 (请注意，如果未为层0指定视图矩形，则矩 `size=`形将与层0矩形相同)。
1. **缩放复合图像** -如果 `catalog::ThumbType=Crop`是，则在仍填充整个视图矩形的同时，将复合图像缩放到尽可能小的图像；额外的图像数据会被裁掉。 如 `catalog::ThumbType= Fit`果是，则合成将缩放到最大图像，同时仍将整个合成适合到视图矩形中。 如 `catalog::ThumbType=Texture`果不缩放合成，则保留中指定的分辨率 `catalog::ThumbRes`。
1. **填充和裁切** -视图矩形中填充了颜 `bgc=` 色(或者，如果未指定，则填充 `attribute::ThumbBkgColor`)。 缩放的复合图像使用以下属性与视图矩形对齐： `ThumbHorizAlign` 和属性： `ThumbVertAlign`. 然后，缩放的合成与填充的视图矩形合并，而无需进一步缩放。 超出视图矩形的复合的任何区域都会被裁掉。

