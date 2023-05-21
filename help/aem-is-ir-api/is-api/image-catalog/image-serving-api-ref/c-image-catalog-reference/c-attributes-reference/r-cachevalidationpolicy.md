---
title: CacheValidationPolicy
description: 伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

伺服器快取驗證原則。 指定伺服器端快取專案驗證的時間。

透過基於到期日的驗證，會定期檢查來源影像是否已變更。 使用目錄型驗證時，來源影像只會在 `catalog::TimeStamp` 值已變更。

使用影像目錄時，建議使用目錄型驗證。 直接參照影像時，應使用過期基準驗證，而不使用影像目錄。

## 屬性 {#section-650cbddd81a24c3b8b70479248a45dc9}

列舉。 0代表選取過期型驗證，1代表選取目錄型快取驗證。

## 默认 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

繼承自 `default::CacheValidationPolicy` 如果未定義或為空。

## 另请参阅 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog：：TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
