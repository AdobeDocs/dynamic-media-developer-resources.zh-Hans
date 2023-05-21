---
description: 影像資料檔案路徑。 指定包含此目錄之影像資料的檔案。
solution: Experience Manager
title: 目錄檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---

# 目錄檔案{#catalogfile}

影像資料檔案路徑。 指定包含此目錄之影像資料的檔案。

影像資料檔案會依指定的順序載入。 若相同 `catalog::Id` 值發生在多個記錄中（在相同或不同的目錄檔案中），最後一個例項優先。

## 屬性 {#section-6da55f145ecd4e31a5de52637a436983}

一或多個文字字串值，以逗號分隔。 可选. 每個值都必須是絕對檔案路徑或相對於目錄資料夾的路徑。

## 默认 {#section-80f91cd7a6b2479ebb310319e9c74da7}

空白，表示此影像目錄不包含任何影像資料。

## 另请参阅 {#section-910b67c5041d44d99a105ad43ff63a37}

[目錄資料欄位](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
