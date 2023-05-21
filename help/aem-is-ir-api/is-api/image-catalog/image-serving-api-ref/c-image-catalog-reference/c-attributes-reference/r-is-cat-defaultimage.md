---
description: 預設回應影像。 指定找不到影像檔案且請求中未指定defaultImage=時，所使用的影像或目錄專案。
solution: Experience Manager
title: 預設影像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# 預設影像{#defaultimage}

預設回應影像。 指定找不到影像檔案且請求中未指定defaultImage=時，所使用的影像或目錄專案。

可以是目錄專案（包括範本）或相對(至 `attribute::RootPath`)或絕對影像檔案路徑。 可用來以預設影像取代遺失的影像。

## 屬性 {#section-b6d8193827c34e5f948792aba8b8daaf}

文字字串。 若指定，必須為有效的 `catalog::Id` 此影像目錄中的值或相對(至 `attribute::RootPath`)或影像伺服器可存取之影像檔案的絕對路徑。

## 限制 {#section-5d8ea872f0b0415fbd3a83410bbcf512}

預設影像機制未涵蓋外部影像來源；如果外部影像來源無效，則會傳回錯誤。

## 默认 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

繼承自 `default::DefaultImage` 若未定義。 如果已定義但為空，即使已定義，預設影像行為也會停用 `default::DefaultImage` 已定義。

## 另请参阅 {#section-dc0fb4e72294442882b33a479fbc2b82}

[屬性：：DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ， [預設影像=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)， [catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)， [attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)， [attribute：：DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
