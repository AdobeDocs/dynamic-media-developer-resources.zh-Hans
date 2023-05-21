---
description: 目錄比對選項。
solution: Experience Manager
title: Fullmatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---

# Fullmatch{#fullmatch}

目錄比對選項。

目錄專案被指定為 `*`rootId`*/ *`imageId`*` HTTP要求中的配對。 剖析時，如果符合下列條件，則會選取目錄 `*`rootId`*` 符合 `attribute::RootId` 目錄的值，而目錄記錄是以相符專案來識別 `*`imageId`*` 搭配 `catalog::Id` 值。 如果找到目錄，但沒有相符的目錄專案 `*`imageId`*`，伺服器可執行下列兩項操作之一：

若 `attribute::FullMatch` 未設定，則伺服器會使用相符目錄的屬性。 在這種情況下， `*`rootId`*` 取代為 `attribute::RootPath` (或 `default::RootPath`，若未在此目錄中指定)。

若 `attribute::FullMatch` 設定時，伺服器會完全忽略目錄（就像沒有相符的目錄一樣），然後繼續使用預設的目錄屬性。 在這種情況下， `*`rootId`*` 保留為路徑的一部分(在前面加上 `default::RootPath`)。

## 屬性 {#section-25e021dbe6574d00aadd08a7fa0b6e81}

标记. 將預設行為設定為0，或將設定為1以啟用完全相符行為。

## 默认 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

繼承自 `default::FullMatch` 如果未定義或為空。

## 另请参阅 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute：：RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ， [catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
