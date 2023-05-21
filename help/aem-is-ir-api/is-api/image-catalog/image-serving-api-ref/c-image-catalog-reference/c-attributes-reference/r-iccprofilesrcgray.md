---
description: 灰階預設輸入色彩設定檔。 指定用於未內嵌色彩設定檔的灰階來源影像，以及用各種「影像伺服」命令（例如color=）指定的某些灰階色彩值的ICC色彩設定檔名稱。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰階預設輸入色彩設定檔。 指定用於未內嵌色彩設定檔的灰階來源影像，以及用各種「影像伺服」命令（例如color=）指定的某些灰階色彩值的ICC色彩設定檔名稱。

## 屬性 {#section-8cbb316df6eb463aaca7b308d3568086}

文字字串。 若指定，則必須為有效 `icc::Name` 值來自此影像目錄或預設目錄的ICC設定檔對映，或是相對於的檔案路徑 `attribute::RootPath`. 參照的ICC設定檔必須是灰階設定檔。

## 默认 {#section-bcc7250715884412bd0780f60d1cce7b}

繼承自 `default::IccProfileSrcGray` 如果未定義或為空。 若 `attribute::IccProfileSrcGray` 無法解析為有效的設定檔， `attribute::IccProfileGray` 會改用。

## 另请参阅 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [attribute：：IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
