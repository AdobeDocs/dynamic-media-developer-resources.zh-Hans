---
description: 相对图像URL的根URL。 指定相对图像URL的根URL。
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# RootUrl{#rooturl}

相对图像URL的根URL。 指定相对图像URL的根URL。

`attribute::RootUrl` 当或值被 `attribute::RootPath` {大 `src=` 括号 `mask=` }或（圆括号）括起来时，将使用。

## 属性 {#section-fe02269b4b724319a5d1f2cfcae31cba}

文本字符串值。 绝对URL根路径，包括前导协议标识符。 支持以下协议：HTTP、HTTPS和FTP。

## 默认 {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

从`default::RootUrl`继承（如果未定义）。 如果已定义但为空，则此图像目录不支持相对URL。

## 另请参阅 {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
