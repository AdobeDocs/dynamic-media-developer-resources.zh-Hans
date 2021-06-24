---
description: 查看图像转换
solution: Experience Manager
title: 查看图像转换
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 查看图像转换{#view-transform-for-images}

响应`req=img`请求返回给客户端的图像是通过考虑以下值从复合图像派生的：`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`和复合图像的大小。

如果指定了`wid=`和`hei=`，但未指定`scl=`，则会缩放复合图像，使其完全符合`wid=`和`hei=`定义的视图方向。 如果视图矩形的宽高比与复合图像的宽高比不同，则缩放的复合图像会使用`align=`值（如果指定）在视图矩形内对齐，否则会居中。 未被图像数据覆盖的任何空间都将填充`bgc=`，或者，如果未指定，则填充`attribute::BkgColor`。

如果指定`scl=`，则复合图像将按该缩放因子缩放。 如果还指定了`wid=`和/或`hei=`，则缩放的图像随后会被裁剪到`wid=`和/或`hei=`，或者根据需要添加额外空间。 `align=` 指定图像被裁剪或添加额外空间的位置，并使用或填充任何额 `bgc=` 外空 `attribute::BkgColor`间。

如果未指定`wid=`、`hei=`和`scl=`，并且复合图像的宽度或高度都超过`attribute::DefaultPix`，则复合图像的缩放比例将不超过`attribute::DefaultPix`。 否则，将不缩放复合图像。

要确保返回视图图像而不进行任何进一步缩放，请指定`scl=1`。

如果指定了`rgn=`，则相应地裁剪回复图像以达到最终的回复图像大小。 此大小与`attribute::MaxPix`（如果已定义）进行比较，如果任一维度中的回复图像较大，则会生成错误。

如果`fmt=`指定的数据没有Alpha，则回复图像中的任何透明区域都将填充`bgc=`或`attribute::BkgColor`。
