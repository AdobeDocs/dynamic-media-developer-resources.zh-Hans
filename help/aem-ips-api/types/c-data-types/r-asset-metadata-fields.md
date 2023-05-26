---
title: AssetMetadataField
description: 返回指定资源类型的元数据字段定义。
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

返回指定资源类型的元数据字段定义。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| 资产类型 | `xsd:string` | 与字段定义关联的资源类型（有关值，请参阅“资源类型”）。 |
| fieldArray | `types:MetadataFieldArray` | 与中指定的资源类型关联的元数据字段定义数组 `assetType`. |
