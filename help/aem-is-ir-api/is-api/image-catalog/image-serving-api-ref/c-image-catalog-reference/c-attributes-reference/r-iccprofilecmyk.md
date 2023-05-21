---
description: CMYK預設輸出色彩設定檔。 指定當沒有以icc=指定輸出色域時，用於CMYK回應影像的ICC色彩設定檔名稱，以及用於以各種「影像伺服」命令（例如color=）指定的某些CMYK色彩值。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK預設輸出色彩設定檔。 指定當沒有以icc=指定輸出色域時，用於CMYK回應影像的ICC色彩設定檔名稱，以及用於以各種「影像伺服」命令（例如color=）指定的某些CMYK色彩值。

## 屬性 {#section-d8b6102cc1c744d482f99808ccfcaa24}

文字字串。 若指定，則必須為有效 `icc::Name` 值來自此影像目錄或預設目錄的ICC設定檔對映，或是相對於的檔案路徑 `attribute::RootPath`. 參照的ICC設定檔必須是CMYK設定檔。

## 默认 {#section-62442df09a724950bfbdd0640b3e6678}

繼承自 `default::IccProfileCmyk` 如果未定義或為空。

## 另请参阅 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [屬性：：IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
