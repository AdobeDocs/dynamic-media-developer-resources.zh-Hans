---
description: 分辨率。 “实际”图像分辨率，通常以每英寸像素数表示，但也可能以其他单位表示，例如每米像素数。
solution: Experience Manager
title: 分辨率
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
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
