---
description: 靜態內容目錄資料檔案路徑。 指定包含此目錄之靜態內容資料的檔案。
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

靜態內容目錄資料檔案路徑。 指定包含此目錄之靜態內容資料的檔案。

靜態內容目錄資料檔案會依照指定的順序載入。 若相同 `static::Id` 值發生在多個記錄中（在相同或不同的目錄檔案中），最後一個例項優先。

## 屬性 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

一或多個文字字串值，以逗號分隔。 可选. 每個值都必須是絕對檔案路徑或相對於目錄資料夾的路徑。

## 默认 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空白，表示此影像目錄不包含任何靜態內容資料。

## 另请参阅 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[目錄資料](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
