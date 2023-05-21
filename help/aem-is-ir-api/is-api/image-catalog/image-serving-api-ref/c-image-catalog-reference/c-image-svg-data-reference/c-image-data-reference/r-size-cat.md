---
description: 图像大小. 目錄「路徑」參照之完整解析度影像的畫素大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 9%

---

# 大小{#size}

图像大小. catalog：：Path參照之全解析度影像的畫素大小。

如果提供此值，「影像伺服」會使用它，以避免必須開啟影像才能取得實際影像大小。

>[!NOTE]
>
>若 `catalog::Size`提供，且與實際完整解析度影像大小不同，可能會導致未定義的行為。

## 屬性 {#section-5c914ec8b1444a8e99d811b647cd42a3}

兩個整數，每個都大於0，以逗號分隔。 可选.

## 默认 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

如果欄位不存在或欄位為空，則會使用影像的實際大小。

## 另请参阅 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog：：Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ， [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
