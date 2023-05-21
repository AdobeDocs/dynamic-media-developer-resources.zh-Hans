---
title: AssetMetadataField
description: 傳回指定資產型別的中繼資料欄位定義。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

傳回指定資產型別的中繼資料欄位定義。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetType | `xsd:string` | 與欄位定義相關聯的資產型別（如需值，請參閱「資產型別」）。 |
| fieldArray | `types:MetadataFieldArray` | 與中指定的資產型別關聯的中繼資料欄位定義陣列 `assetType`. |
