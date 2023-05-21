---
description: 預設影像檔案字尾。 如果路徑不包含檔案字尾，則附加至目錄Path （或目錄MaskPath）欄位值
solution: Experience Manager
title: 預設分機
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# 預設分機{#defaultext}

預設影像檔案字尾。 附加至目錄：：Path （或catalog：：MaskPath）欄位值（如果路徑不包含檔案字尾）

檔案字尾由句點和一個或多個字元組成，介於句點和字串結尾之間。 如果路徑未解析為目錄專案，且最後一個路徑元素不包含檔案字尾，則會將字尾附加至http路徑。

## 屬性 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

文字字串。 必須包含前導的「。」 和一個或多個字元。

## 默认 {#section-1194c36ffe0748c5b9ff7d732a506588}

繼承自 `default::DefaultExt` 若未定義。 如果已定義但空白，則使用此目錄時，預設字尾不會套用至影像名稱。

## 另请参阅 {#section-d7c408b979844643adff8258f500eb7c}

[catalog：：Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ， [catalog：：MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
