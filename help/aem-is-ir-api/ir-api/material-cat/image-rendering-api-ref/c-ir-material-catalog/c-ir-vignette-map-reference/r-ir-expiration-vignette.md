---
description: 使用者端快取存留時間。 到期前的小時數。 用於管理使用者端和Proxy伺服器快取。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# 過期{#expiration}

使用者端快取存留時間。 到期前的小時數。 用於管理使用者端和Proxy伺服器快取。

另請參閱 [catalog：：到期](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md) 以取得詳細資訊。

## 屬性 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

實數、-2、-1、0或更大。 從產生回應影像到到期為止的小時數。 設為0可一律使回應影像立即過期，以有效停用使用者端快取。 設為–1以標籤為 `never expire`；在此情況下，伺服器一律會傳回403狀態來回應條件 `GET` 會要求但不檢查檔案是否已實際變更。 設定為–2會使用所提供的預設值 `attribute::Expiration`.

## 默认 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 如果欄位不存在、值是–2或欄位為空，則會使用。

## 另请参阅 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ， [catalog：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)， [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
