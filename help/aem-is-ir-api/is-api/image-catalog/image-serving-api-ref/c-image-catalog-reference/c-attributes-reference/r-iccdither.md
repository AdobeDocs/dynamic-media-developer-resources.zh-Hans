---
description: 颜色转换抖动。 指定在通过icc=未做出明确选择时，是否应使用仿色来提高颜色转换的感知质量。
solution: Experience Manager
title: Icc仿色
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4b444f0f-2313-4477-8a22-7840b4783c88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 3%

---

# Icc仿色{#iccdither}

颜色转换抖动。 指定在通过icc=未做出明确选择时，是否应使用仿色来提高颜色转换的感知质量。

## 属性 {#section-b7ba44d2d5de43f5a0841fe4cac29d35}

标志。 设置为0表示禁用或设置为1表示启用仿色。

## 默认 {#section-86c4230a16454464880f64d4ab5ad533}

如果未定义或为空，则从`default::IccDither`继承。

## 另请参阅 {#section-fe119006eb414a618b6ec9edbed8fe94}

[属性：：IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md) &#42;，[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
