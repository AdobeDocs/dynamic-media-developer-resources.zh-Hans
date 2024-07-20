---
description: 图像的视图转换
solution: Experience Manager
title: 图像的视图转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 图像的视图转换{#view-transform-for-images}

通过考虑以下值，从复合图像派生了响应`req=img`请求返回到客户端的图像： `wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`以及复合图像的大小。

如果指定了`wid=`和`hei=`，但未指定`scl=`，则将缩放复合图像以使其完全适合由`wid=`和`hei=`定义的视图矩形。 如果视图矩形的长宽比不同于复合图像的长宽比，则使用`align=`值（如果已指定）在视图矩形内对齐缩放的复合图像，否则将其居中。 图像数据未覆盖的任何空间将以`bgc=`填充，如果未指定，则以`attribute::BkgColor`填充。

如果指定了`scl=`，则复合图像将按该缩放因子进行缩放。 如果还指定了`wid=`和/或`hei=`，则缩放的图像将裁剪为`wid=`和/或`hei=`，或者根据需要添加额外的空间。 `align=`指定在何处裁切图像或添加额外空间，任何额外空间都用`bgc=`或`attribute::BkgColor`填充。

如果未指定`wid=`、`hei=`和`scl=`，并且复合图像的宽度或高度超过`attribute::DefaultPix`，则复合图像将缩放为不超过`attribute::DefaultPix`。 否则，不使用缩放使用复合图像。

要确保返回视图图像而不进行任何进一步的缩放，请指定`scl=1`。

如果指定了`rgn=`，则回复图像将相应地被裁剪以得到最终的回复图像大小。 将此大小与`attribute::MaxPix`（如果已定义）进行比较，如果任一维度中的回复图像较大，则会生成错误。

如果`fmt=`指定了不含Alpha的数据，则回复图像中的任何透明区域都将使用`bgc=`或`attribute::BkgColor`填充。
