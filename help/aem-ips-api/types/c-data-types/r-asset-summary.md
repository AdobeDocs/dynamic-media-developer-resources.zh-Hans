---
description: 包含有关资源的汇总信息的元数据搜索结果。
solution: Experience Manager
title: 资产摘要
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# [!DNL AssetSummary]{#assetsummary}

包含有关资源的汇总信息的元数据搜索结果。

语法

## 参数 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 资源句柄。 |
| 类型 | `xsd:string` | 资源类型. “资产类型”常量定义可能的值。 可选. |
| 名称 | `xsd:string` | 资源名称。 可选. |
| 文件夹 | `xsd:string` | 包含资产的文件夹。 |
| 文件名 | `xsd:string` | 资源的文件名。 |
| 已创建 | `xsd:dateTime` | 资源创建日期。 |
| createUser | `xsd:string` | 创建资源的用户。 |
| lastModified | `xsd:dateTime` | 上次更新资产的日期。 |
| lastModifyUser | `xsd:string` | 上次修改资源的用户。 |
| metadataArray | `types:MetadataArray` | 与资源关联的元数据值数组。 |
| 分数 | `xsd:double` | 定义相似性搜索时的精度（0 =无匹配，1 =完全匹配）。 |
| scoredetail | `xsd:string` | 作为相似性搜索的结果，保存有关相似区域的详细信息。 |
