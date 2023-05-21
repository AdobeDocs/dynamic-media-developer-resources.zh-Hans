---
description: 預設縮圖解析度。 提供縮圖物件解析度的預設值，以防止特定目錄記錄未包含有效的目錄ThumbRes值。
solution: Experience Manager
title: 縮圖
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# 縮圖{#thumbres}

預設縮圖解析度。 提供縮圖物件解析度的預設值，以防止特定目錄記錄未包含有效的目錄：：ThumbRes值。

僅用於縮圖要求( `req=tmb`)和時間 `catalog::ThumbType=3`.

## 屬性 {#section-88d37d0e030f4879a9e584dd2cc780f3}

實數，大於0。通常以畫素/英吋表示，但也可能是其他單位，例如每米的畫素。

## 默认 {#section-86588899ec9b4276a98b03d7faf64003}

繼承自 `default::ThumbRes` 如果未定義或為空。

## 另请参阅 {#section-a6d2cce2e404441a996dba98a95c8e16}

[目錄：：ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
