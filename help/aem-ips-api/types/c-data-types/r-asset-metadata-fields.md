---
title: AssetMetadataFields
description: 返回指定资产类型的元数据字段定义。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# AssetMetadataFields{#assetmetadatafields}

返回指定资产类型的元数据字段定义。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetType | `xsd:string` | 与字段定义关联的资产类型（有关值，请参阅“资产类型”）。 |
| fieldArray | `types:MetadataFieldArray` | 与中指定的资产类型关联的元数据字段定义数组 `assetType`. |
