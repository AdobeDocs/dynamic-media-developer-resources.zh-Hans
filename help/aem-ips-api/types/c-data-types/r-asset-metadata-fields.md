---
description: 返回指定资产类型的元数据字段定义。
seo-description: 返回指定资产类型的元数据字段定义。
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Scene7 Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetMetadataFields{#assetmetadatafields}

返回指定资产类型的元数据字段定义。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`assetType`*` | `xsd:string` | 与字段定义关联的资产类型（有关值，请参阅“资产类型”）。 |
| ` *`fieldArray`*` | `types:MetadataFieldArray` | 与中指定的资产类型关联的元数据字段定义的数组 `assetType`。 |

