---
description: 视图变换图像
solution: Experience Manager
title: 视图变换图像
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 图像的视图变换{#view-transform-for-images}

响应`req=img`请求返回给客户端的映像是从复合映像派生的，方法是考虑以下值：`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`和复合图像的大小。

如果指定了`wid=`和`hei=`，但未指定`scl=`，则会缩放复合图像，使其完全适合由`wid=`和`hei=`定义的视图矩形。 如果视图矩形的长宽比与复合图像的长宽比不同，则使用`align=`值（如果指定）在视图矩形内对齐缩放的复合图像，否则将居中对齐。 未被图像数据覆盖的任何空间都用`bgc=`填充，如果未指定，则用`attribute::BkgColor`填充。

如果指定`scl=`，则复合图像将按该缩放因子进行缩放。 如果还指定了`wid=`和/或`hei=`，则会根据需要将缩放的图像裁剪到`wid=`和/或`hei=`，或添加额外的空间。 `align=` 指定裁剪图像或添加额外空间的位置，并使用或填充任何额外 `bgc=` 空间 `attribute::BkgColor`。

如果既未指定`wid=`、`hei=`也未指定`scl=`，并且复合图像的宽度或高度超过`attribute::DefaultPix`，则复合图像将缩放为不超过`attribute::DefaultPix`。 否则，将不使用缩放功能来使用合成图像。

要确保返回视图图像时不进行任何进一步缩放，请指定`scl=1`。

如果指定`rgn=`，则相应地裁剪回复图像以得出最终的回复图像大小。 将此大小与`attribute::MaxPix`（如果已定义）进行比较，如果回复图像在任一维度中较大，则会生成错误。

如果`fmt=`指定没有Alpha的数据，则返回图像中的所有透明区域都用`bgc=`或`attribute::BkgColor`填充。
