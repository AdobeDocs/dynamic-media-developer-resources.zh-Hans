---
title: CacheValidationPolicy
description: 伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。

透過到期日式驗證，會定期檢查原始資料和暈映，以檢視它們是否已變更。 使用目錄型驗證時，來源影像只會在 `catalog::TimeStamp` 值已變更。

同時使用材質和暈映目錄時，建議使用目錄型驗證。 當路徑直接在影像演算請求中參考暈映時，應使用到期型驗證。

## 屬性 {#section-46e13cb341eb442c86e0d8292de23ea0}

列舉。 0以選取以到期日為基礎的驗證。 1以選取目錄型快取驗證。

## 默认 {#section-e09f3af8b6b3497d963199988dc5345d}

繼承自 `default::CacheValidationPolicy` 如果未定義或為空。

## 另请参阅 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
