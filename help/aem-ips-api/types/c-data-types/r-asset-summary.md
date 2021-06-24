---
description: 包含有关资产的摘要信息的元数据搜索结果。
solution: Experience Manager
title: 资产摘要
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 11%

---

# 资产摘要{#assetsummary}

包含有关资产的摘要信息的元数据搜索结果。

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
| `*`lastModifyUser`*` | `xsd:string` | 修改资产的最后一个用户。 |
| `*`metadataArray`*` | `types:MetadataArray` | 与资产关联的元数据值数组。 |
| `*`分数`*` | `xsd:double` | 在进行相似性搜索时定义精度（0 =无匹配，1 =精确匹配）。 |
| `*`scoreDetail`*` | `xsd:string` | 包含有关相似区域作为相似性搜索结果的详细信息。 |
