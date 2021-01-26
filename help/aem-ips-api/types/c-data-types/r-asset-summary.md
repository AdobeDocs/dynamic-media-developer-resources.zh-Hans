---
description: 包含资产摘要信息的元数据搜索结果。
seo-description: 包含资产摘要信息的元数据搜索结果。
seo-title: 资产摘要
solution: Experience Manager
title: 资产摘要
topic: Dynamic Media Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 11%

---


# 资产摘要{#assetsummary}

包含资产摘要信息的元数据搜索结果。

语法

## 参数 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 资产句柄。 |
| `*`类型`*` | `xsd:string` | 资源类型. “资产类型”常量定义可能的值。 可选。 |
| `*`name`*` | `xsd:string` | 资产名称。 可选。 |
| `*`文件夹`*` | `xsd:string` | 包含资产的文件夹。 |
| `*`文件名`*` | `xsd:string` | 资产的文件名。 |
| `*`created`*` | `xsd:dateTime` | 资产创建日期。 |
| `*`createUser`*` | `xsd:string` | 创建资产的用户。 |
| `*`lastModified`*` | `xsd:dateTime` | 资产上次更新的日期。 |
| `*`lastModifyUser`*` | `xsd:string` | 上次修改资产的用户。 |
| `*`metadataArray`*` | `types:MetadataArray` | 与资产关联的元数据值的数组。 |
| `*`分数`*` | `xsd:double` | 定义相似性搜索时的精度（0 =无匹配，1 =精确匹配）。 |
| `*`scoreDetail`*` | `xsd:string` | 保存作为相似性搜索结果的类似区域的详细信息。 |

