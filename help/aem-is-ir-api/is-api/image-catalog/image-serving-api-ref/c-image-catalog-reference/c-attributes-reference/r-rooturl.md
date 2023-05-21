---
description: 相對影像URL的根URL。 指定相對影像URL的根URL。
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# RootUrl{#rooturl}

相對影像URL的根URL。 指定相對影像URL的根URL。

`attribute::RootUrl` 已使用，而不是 `attribute::RootPath` 當 `src=` 或 `mask=` 值由{curly braces}或（括弧）括住。

## 屬性 {#section-fe02269b4b724319a5d1f2cfcae31cba}

文字字串值。 絕對URL根路徑，包括前導通訊協定識別碼。 支援下列通訊協定：HTTP、HTTPS和FTP。

## 默认 {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

繼承自 `default::RootUrl` 若未定義。 如果已定義但空白，則此影像目錄不支援相對URL。

## 另请参阅 {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [attribute：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)， [規則集：：PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
