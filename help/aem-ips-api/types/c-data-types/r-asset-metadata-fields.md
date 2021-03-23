---
description: 返回指定资产类型的元数据字段定义。
seo-description: 返回指定资产类型的元数据字段定义。
seo-title: 资产元数据字段
solution: Experience Manager
title: 资产元数据字段
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Media Classic，SDK/API，元数据，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---


# AssetMetadataFields{#assetmetadatafields}

返回指定资产类型的元数据字段定义。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetType`*` | `xsd:string` | 与字段定义关联的资产类型（有关值，请参阅“资产类型”）。 |
| `*`fieldArray`*` | `types:MetadataFieldArray` | 与`assetType`中指定的资产类型关联的元数据字段定义的数组。 |

