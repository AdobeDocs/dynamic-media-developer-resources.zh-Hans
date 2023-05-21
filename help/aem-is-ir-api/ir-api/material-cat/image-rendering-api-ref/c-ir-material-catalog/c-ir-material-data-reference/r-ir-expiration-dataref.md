---
title: 過期
description: 使用者端快取存留時間。 到期前的小時數。 用於管理使用者端和Proxy伺服器快取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# 過期{#expiration}

使用者端快取存留時間。 到期前的小時數。 用於管理使用者端和Proxy伺服器快取。

伺服器會將此值與傳輸時間/日期相加，以計算NTTP回應資料的到期時間/日期。

瀏覽器會使用檔案的到期時間來管理快取。 將請求傳遞至伺服器之前，瀏覽器會檢查其快取，檢視檔案是否已下載。 若是如此，且檔案尚未過期，瀏覽器會傳送條件式GET要求（例如包含If-Modified-Since HTTP要求標頭），而非一般GET要求。 伺服器可以選擇以「304」狀態回應，而不傳輸影像。 瀏覽器隨即會從其快取載入檔案。 這可能會大幅提升經常存取資料的整體效能。

伺服器會將expires HTTP回應標頭設定為目前的日期/時間，加上暈映：：Expiration和所有catalog：：Expiration值的最小值，以取得暈映和轉譯作業中涉及的所有材質。

有效期主要是為影像資料回應所設定。 某些型別的回應一律會標籤為立即過期（或標籤為不可快取），包括所有錯誤回應或屬性回覆。

## 屬性 {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

實數、-2、-1、0或更大。 從產生回應影像到到期為止的小時數。 設為0可一律使回應影像立即過期，以有效停用使用者端快取。 設為–1以標籤為 `never expire`. 在此情況下，伺服器一律會傳回304狀態（未修改）以回應條件 `GET` 會要求但不檢查檔案是否已實際變更。 設定為–2會使用所提供的預設值 `attribute::Expiration`.

## 默认 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` 如果欄位不存在、值是–2或欄位為空，則會使用。

## 另请参阅 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ， [暈映：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)， [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
