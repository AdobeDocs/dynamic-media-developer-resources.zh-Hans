---
description: 图像锚点。 来源点：将此图像用作模板或复合图像中的图层。
seo-description: 图像锚点。 来源点：将此图像用作模板或复合图像中的图层。
seo-title: 锚点
solution: Experience Manager
title: 锚点
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# 锚点{#anchor}

图像锚点。 来源点：将此图像用作模板或复合图像中的图层。

还定义旋转的默认中心点。

## 属性 {#section-95740f14160744e7bc763094b8be40d8}

两个整数，以逗号分隔。 相对于全分辨率图像左上角的像素偏移。

由(而 `anchor=`后者又可以由覆盖 `origin=`)覆盖。

## 默认 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此字段不存在或为空，并且这是有效的图像记录（即，如果有效），则使用图像的中 `catalog::Path` 心点。

## 另请参阅 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [来源=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
