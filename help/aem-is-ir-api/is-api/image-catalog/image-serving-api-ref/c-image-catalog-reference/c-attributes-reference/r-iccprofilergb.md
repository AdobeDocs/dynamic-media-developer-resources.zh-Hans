---
description: RGB預設輸出色彩設定檔。 指定當沒有以icc=指定輸出色域時，用於RGB回應影像的ICC色彩設定檔名稱，以及用於以各種「影像伺服」命令（例如color=）指定的某些RGB色彩值。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB預設輸出色彩設定檔。 指定當沒有以icc=指定輸出色域時，用於RGB回應影像的ICC色彩設定檔名稱，以及用於以各種「影像伺服」命令（例如color=）指定的某些RGB色彩值。

## 屬性 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

文字字串。 若指定，則必須為有效 `icc::Name` 值來自此影像目錄或預設目錄的ICC設定檔對映，或是相對於的檔案路徑 `attribute::RootPath`. 參考的ICC設定檔必須是RGB設定檔。

## 默认 {#section-dfe08dd7b851453ca816623a4179955b}

繼承自 `default::IccProfileRgb` 如果未定義或為空。

## 另请参阅 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [attribute：：IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
