---
description: 锐化图像。 对图层或最终视图图像应用基本锐化滤镜（如果layer=comp），在进行所有缩放后。
seo-description: 锐化图像。 对图层或最终视图图像应用基本锐化滤镜（如果layer=comp），在进行所有缩放后。
seo-title: op_sharpen
solution: Experience Manager
title: op_sharpen
uuid: 1a00c60a-0d5c-4a99-a649-f29ebd710cf3
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 7%

---


# op_sharpen{#op-sharpen}

锐化图像。 对图层或最终视图图像应用基本锐化滤镜（如果layer=comp），在进行所有缩放后。

`op_sharpen=0|1`

图层蒙版或复合蒙版也会进行锐化。

## 属性 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

图层属性或视图属性。 应用于当前图层或最终视图图像（如果`layer=comp`）。 被效果图层忽略。

## 默认 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`，以获得无锐化效果。

## 示例 {#section-3202122df5db4e14b358ecabfb6d8b85}

补偿由图像重新取样引起的轻微模糊。 我们还会提高JPEG质量，以避免沿着锐化的边缘出现其他JPEG伪像。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 另请参阅 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
