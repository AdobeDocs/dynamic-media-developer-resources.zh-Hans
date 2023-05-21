---
description: 浮水印選取器。 指定要用作浮水印影像或範本的目錄記錄的目錄ID。
solution: Experience Manager
title: 浮水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# 浮水印{#watermark}

浮水印選取器。 指定要用作浮水印影像或範本的目錄記錄的目錄：：Id。

若指定，伺服器會將浮水印套用至所有影像要求的影像資料( `req=img`)。

## 屬性 {#section-fad6ffff4c5f4b5c8010281bc1377055}

文字字串。 若指定，則必須為有效 `Catalog::Id` 值(或預設目錄中的值，若在 [!DNL default.ini])。

## 默认 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

繼承自 `default::Watermark` 若未定義。 如果已定義但為空，則不會對此影像目錄套用浮水印，即使 `default::Watermark` 已定義。

## 另请参阅 {#section-f15dbe31013849828d78588742dde58e}

[catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
