---
description: 缩览图的垂直对齐。 指定在由wid=和hei=或属性DefaultThumbPix指定的回复图像矩形中缩略图的垂直对齐方式。
seo-description: 缩览图的垂直对齐。 指定在由wid=和hei=或属性DefaultThumbPix指定的回复图像矩形中缩略图的垂直对齐方式。
seo-title: ThumbVertAlign
solution: Experience Manager
title: ThumbVertAlign
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a90281eb-9681-4b4a-a94b-663f007fb32f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# ThumbVertAlign{#thumbvertalign}

缩览图的垂直对齐。 指定在由wid=和hei=或属性：:DefaultThumbPix指定的回复图像矩形中缩略图的垂直对齐方式。

仅用于缩略图请求(`req=tmb`)。

## 属性 {#section-f02c23248e87419caf3d95add51aea1e}

枚举。 允许的值分别为1、2和3（对于顶部对齐、居中对齐和底部对齐）。

## 默认 {#section-30caa4e772254419ad7a3a89d440666c}

如果未定义或为空，则从`default::ThumbHorizAlign`继承。

## 另请参阅 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[catalog::ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) , [属性：:DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
