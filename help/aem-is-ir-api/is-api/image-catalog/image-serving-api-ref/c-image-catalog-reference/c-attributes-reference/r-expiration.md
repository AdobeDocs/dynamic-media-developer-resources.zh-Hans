---
description: 預設使用者端快取存留時間。 提供預設到期間隔，以防止特定目錄記錄未包含有效的目錄Expiration值。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---

# 過期{#expiration}

預設使用者端快取存留時間。 提供預設到期時間間隔，以防止特定目錄記錄未包含有效的目錄：：Expiration值。

## 屬性 {#section-063be3b2f13a48a3a5ab8080718e9812}

實數，0或更大。 自回覆資料產生至到期為止的小時數。 設為0可一律使回覆影像立即過期，以有效停用使用者端快取。 設為–1以標籤為 `never expire`.

## 默认 {#section-f55308b195c04083996f6717c8537634}

繼承自 `default::Expiration` 如果未定義或為空。

TTL （存留時間）是快取過期前的持續時間。 預設TTL為10小時。

## 另请参阅 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [attribute：：DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)， [attribute：：NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
