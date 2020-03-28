---
description: 'null'
seo-description: 'null'
seo-title: 视图变换图像
solution: Experience Manager
title: 视图变换图像
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 视图变换图像{#view-transform-for-images}

响应请求返回给客户端的图像是 `req=img` 从合成图像中考虑以下值得来的： `wid=`、 `hei=`、 `fit=`、 `scl=`、 `rgn=`和 `attribute::DefaultPix``attribute::MaxPix`复合图像的大小。

如果 `wid=` 指定 `hei=` 了并且未指定，则会缩 `scl=` 放复合图像，以便它完全适合和定义的视图矩 `wid=` 形 `hei=`。 如果视图矩形的长宽比与合成图像的长宽比不同，则使用值（如果指定）在视图矩形内对齐缩放的复合图像，否则，将居中对齐。 `align=` 未被图像数据覆盖的任何空间都将 `bgc=` 填充，或者（如果未指定）填充 `attribute::BkgColor`。

如果 `scl=` 指定，则复合图像会按该缩放因子缩放。 如果 `wid=` 也指定和/ `hei=` 或，则缩放后的图像会根据需要裁剪到 `wid=` 和／或添 `hei=` 加额外的空间。 `align=` 指定裁剪图像或添加额外空间的位置，并使用或填充任何额外 `bgc=` 空间 `attribute::BkgColor`。

如果既 `wid=`未指定 `hei=` ，也未指 `scl=` 定，并且如果复合图像的宽度或高度超过此值，则复合图像将缩放为不超过 `attribute::DefaultPix``attribute::DefaultPix`。 否则，将不使用缩放功能来使用合成图像。

要确保返回视图图像而不进行任何进一步缩放，请指定 `scl=1`。

如果 `rgn=` 指定了回复图像，则相应地裁剪回复图像以达到最终的回复图像大小。 将比较此大小(如果已定 `attribute::MaxPix` 义)，并且如果回复图像在任一维度中较大，则会生成错误。

如果 `fmt=` 指定不带alpha的数据，则返回图像中的任何透明区域都将填充 `bgc=` 或 `attribute::BkgColor`。
