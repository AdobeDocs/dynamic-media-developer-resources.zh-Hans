---
description: 锐化图像。 如果layer=comp，则在进行所有缩放后，将基本锐化滤镜应用于图层或最终视图图像。
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# op_sharpen{#op-sharpen}

锐化图像。 如果layer=comp，则在进行所有缩放后，将基本锐化滤镜应用于图层或最终视图图像。

`op_sharpen=0|1`

图层蒙版或复合蒙版也会被锐化。

## 属性 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

层属性或视图属性。 如果`layer=comp`，则应用于当前层或最终视图图像。 被效果层忽略。

## 默认 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`，无锐化效果。

## 示例 {#section-3202122df5db4e14b358ecabfb6d8b85}

补偿由图像重新取样引起的轻微模糊。 我们还会提高JPEG质量，以避免沿锐化的边缘出现其他JPEG伪影。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 另请参阅 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
