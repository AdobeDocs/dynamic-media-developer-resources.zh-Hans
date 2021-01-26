---
description: 图像锚点。 来源此图像用作模板或复合图像中的图层时的点。
seo-description: 图像锚点。 来源此图像用作模板或复合图像中的图层时的点。
seo-title: 锚点
solution: Experience Manager
title: 锚点
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# 锚点{#anchor}

图像锚点。 来源此图像用作模板或复合图像中的图层时的点。

还定义旋转的默认中心点。

## 属性 {#section-95740f14160744e7bc763094b8be40d8}

两个整数，以逗号分隔。 相对于全分辨率图像的左上角的像素偏移。

由`anchor=`覆盖（而`origin=`又可以覆盖）。

## 默认 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此字段不存在或为空，并且这是有效的图像记录（即，如果`catalog::Path`有效），则使用图像的中心点。

## 另请参阅 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [来源=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
