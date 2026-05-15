---
title: op_sharpen
description: 锐化图像。 如果图层=comp，则在全部缩放后将基本锐化滤镜应用于图层或最终视图图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
TQID: 'https://experienceleague.adobe.com/CLyNZKJir4mYZ2L04ZKpnkNk6LX9xs8VUwnwwPrs-Zc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 3%

---

# op_sharpen{#op-sharpen}

锐化图像。 如果图层=comp，则在全部缩放后将基本锐化滤镜应用于图层或最终视图图像。

`op_sharpen=0|1`

图层蒙版或复合蒙版也被锐化。

## 属性 {#section-b27f3f6a27c34233b3f76805e18b2aa7}

图层属性或视图属性。 应用于当前图层或最终视图图像（如果`layer=comp`）。 被效果层忽略。

## 默认 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`，无锐化效果。

## 示例 {#section-3202122df5db4e14b358ecabfb6d8b85}

补偿由图像重新取样引起的轻微模糊。 我们还提高了JPEG质量，以避免锐化边缘出现额外的JPEG伪像。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 另请参阅 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ，[op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
