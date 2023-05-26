---
description: 图像的视图转换
solution: Experience Manager
title: 图像的视图转换
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 图像的视图转换{#view-transform-for-images}

响应一个返回给客户端的图像 `req=img` 请求是通过考虑以下值从复合图像派生的： `wid=`， `hei=`， `fit=`， `scl=`， `rgn=`， `attribute::DefaultPix`， `attribute::MaxPix`以及复合图像的大小。

如果 `wid=` 和 `hei=` 已指定，并且 `scl=` 不可以缩放复合图像，使其完全适合由定义的视图矩形 `wid=` 和 `hei=`. 如果视图矩形的长宽比不同于复合图像的长宽比，则使用缩放的复合图像在视图矩形内对准 `align=` 值（如果已指定），否则会居中。 任何未被图像数据覆盖的空间都将被填充 `bgc=` 如果未指定，则使用 `attribute::BkgColor`.

如果 `scl=` 指定时，复合图像将按该缩放因子进行缩放。 如果 `wid=` 和/或 `hei=` 指定缩放图像后，将裁剪到 `wid=` 和/或 `hei=` 或根据需要添加额外的空间。 `align=` 指定在何处裁切图像或添加额外空间，并填充任何额外空间 `bgc=` 或 `attribute::BkgColor`.

如果两者都不 `wid=`， `hei=` 也不 `scl=` 指定，并且如果复合图像的宽度或高度超过 `attribute::DefaultPix`，则复合图像将缩放为不超过 `attribute::DefaultPix`. 否则，将使用该复合图像而不进行缩放。

要确保返回视图图像而不进行任何进一步的缩放，请指定 `scl=1`.

如果 `rgn=` 然后相应地裁剪回复图像以得到最终的回复图像大小。 将此大小与 `attribute::MaxPix` （如果已定义），并且如果回复图像在任一维度中较大，则会生成错误。

如果 `fmt=` 指定不含Alpha的数据，回复图像中的任何透明区域都将填充 `bgc=` 或 `attribute::BkgColor`.
