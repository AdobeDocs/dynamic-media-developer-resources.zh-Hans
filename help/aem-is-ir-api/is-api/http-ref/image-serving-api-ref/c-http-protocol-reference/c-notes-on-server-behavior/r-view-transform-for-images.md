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

响应时返回到客户端的图像 `req=img` 请求是通过考虑以下值从复合图像派生的： `wid=`， `hei=`， `fit=`， `scl=`， `rgn=`， `attribute::DefaultPix`， `attribute::MaxPix`以及复合图像的大小。

如果 `wid=` 和 `hei=` 已指定，并且 `scl=` 不可以，将缩放复合图像，使其完全适合由定义的视图矩形 `wid=` 和 `hei=`. 如果视角的纵横比不同于合成图像的纵横比，则使用缩放的合成图像在视角内对准 `align=` 值（如果已指定），否则居中。 任何未被图像数据覆盖的空间都将被填充 `bgc=` 如果未指定，则使用 `attribute::BkgColor`.

如果 `scl=` 指定后，复合图像将按该缩放因子进行缩放。 如果 `wid=` 和/或 `hei=` 同时指定，然后将缩放的图像裁剪到 `wid=` 和/或 `hei=` 或根据需要添加额外空间。 `align=` 指定在何处裁剪图像或添加额外空间，并用填充任何额外空间 `bgc=` 或 `attribute::BkgColor`.

如果两者均不 `wid=`， `hei=` 也不 `scl=` 指定，并且如果复合图像的宽度或高度超过 `attribute::DefaultPix`，然后缩放复合图像以不超过 `attribute::DefaultPix`. 否则，不使用缩放使用复合图像。

要确保返回视图图像而不进行任何进一步的缩放，请指定 `scl=1`.

如果 `rgn=` 然后相应地裁剪回复图像以得到最终的回复图像大小。 将此大小与 `attribute::MaxPix` （如果已定义），并且如果回复图像在任一维度中较大，则会生成错误。

如果 `fmt=` 指定不带alpha的数据，回复图像中的任何透明区域都填充 `bgc=` 或 `attribute::BkgColor`.
