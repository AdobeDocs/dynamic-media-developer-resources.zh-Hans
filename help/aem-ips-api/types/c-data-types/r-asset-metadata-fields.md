---
description: 返回指定资产类型的元数据字段定义。
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic，SDK/API，元数据，资产管理
role: Developer,Administrator
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# AssetMetadataFields{#assetmetadatafields}

返回指定资产类型的元数据字段定义。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | 与字段定义关联的资产类型（有关值，请参阅“资产类型”）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | 与`assetType`中指定的资产类型关联的元数据字段定义数组。 |
