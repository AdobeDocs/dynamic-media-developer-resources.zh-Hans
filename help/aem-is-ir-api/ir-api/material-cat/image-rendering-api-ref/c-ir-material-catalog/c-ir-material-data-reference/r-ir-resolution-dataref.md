---
description: 分辨率。 “实际”图像分辨率，通常以每英寸像素数表示，但也可能以其他单位表示，例如每米像素数。
solution: Experience Manager
title: 分辨率
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
TQID: 'https://experienceleague.adobe.com/EV1kiy21nLXMKmrDDBQclvZvdB-h-zi9SCkskvzUJNQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 4%

---

# 分辨率{#resolution}

分辨率。 “实际”图像分辨率，通常以每英寸像素数表示，但也可能以其他单位表示，例如每米像素数。

## 属性 {#section-985ca2ad858c4e9c9cbb303f55447553}

实数，大于0。 对于纹理和贴花材料是必需的，除非图像分辨率与attribute：：Resolution相同。 已被纯色和机箱材料忽略。

## 默认 {#section-b1d044e211194242a900aaef4a8c8e6f}

如果字段不存在、值为0或负值或者字段为空，则使用`attribute::Resolution`。

## 另请参阅 {#section-2d04df523d7345f6929178cbc637da78}

[attribute：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ， [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
