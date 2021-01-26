---
description: 返回指定资产类型的元数据字段定义。
seo-description: 返回指定资产类型的元数据字段定义。
seo-title: 资产元数据字段
solution: Experience Manager
title: 资产元数据字段
topic: Dynamic Media Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

返回指定资产类型的元数据字段定义。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`资产类型`*` | `xsd:string` | 与字段定义关联的资产类型（有关值，请参阅“资产类型”）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | 与`assetType`中指定的资产类型关联的元数据字段定义的数组。 |

