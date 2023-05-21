---
description: 預設影像回應的使用者端快取TTL。 提供預設影像回應（傳回以defaultImage=或屬性DefaultImage指定的預設影像的回應）的到期間隔。
solution: Experience Manager
title: 預設過期時間
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---

# 預設過期時間{#defaultexpiration}

預設影像回應的使用者端快取TTL。 提供預設影像回應（傳回以defaultImage=或attribute：：DefaultImage指定的預設影像的回應）的到期間隔。

僅當預設影像未與目錄記錄關聯或預設影像目錄記錄未提供特定時套用 `catalog::Expiration` 值。

## 屬性 {#section-e564512476604fd7b964f9f2903d6d33}

實數，0或更大。 自回覆資料產生至到期為止的小時數。 設為0可一律使回覆影像立即過期，這會有效停用預設影像回應的使用者端快取。 設定為 `-1` 若要標籤為 `never expire`.

## 默认 {#section-131cd32c2e214391857dba5af321f8cd}

繼承自 `default::DefaultExpiration` 如果未定義或為空。

TTL （存留時間）是快取過期前的持續時間。 預設TTL為1小時。

## 另请参阅 {#section-d8642c22e3d947129367dd76366963d6}

[catalog：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [attribute：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
