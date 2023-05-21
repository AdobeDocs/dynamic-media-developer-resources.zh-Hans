---
title: 過期
description: 預設使用者端快取存留時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---

# 過期{#expiration}

預設使用者端快取存留時間。 提供預設過期時間間隔，以防止特定目錄記錄未包含有效的目錄 `catalog::Expiration` 或 `vignette::Expiration` 值。 或者，如果直接存取暈映檔案或材料檔案，而不是透過目錄記錄。

## 屬性 {#section-8e2bade105ec4905ae5c4911f500279f}

實數， `0` 或更高。 自回覆資料產生至到期為止的小時數。 設定為 `0` 讓回覆影像一律立即過期，以有效停用使用者端快取。 設定為 `-1` 若要標籤為 *永不過期*.

## 默认 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

繼承自 `default::Expiration` 如果未定義或為空。

## 另请参阅 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ， [暈映：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
