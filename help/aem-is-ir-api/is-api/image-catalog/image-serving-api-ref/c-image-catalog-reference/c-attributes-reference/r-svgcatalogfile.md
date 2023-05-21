---
description: SVG資料檔案路徑。 指定包含此目錄SVG資料的檔案。
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# SvgCatalogFile{#svgcatalogfile}

SVG資料檔案路徑。 指定包含此目錄SVG資料的檔案。

SVG資料檔案會依指定的確切順序載入到所有影像資料檔案之後。 若相同 `catalog::Id` 值發生於多個記錄中(相同或不同的影像或SVG目錄檔案中)，最後的執行個體優先。

## 屬性 {#section-fc2d549f76474792837b2b92ec2087ea}

一或多個文字字串值，以逗號分隔。 可选. 每個值都必須是絕對檔案路徑或相對於目錄資料夾的路徑。

## 默认 {#section-a4e58951f3c249599665b823566433c9}

空白，表示此影像目錄不包含任何SVG資料。

## 另请参阅 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)， [目錄檔案](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
