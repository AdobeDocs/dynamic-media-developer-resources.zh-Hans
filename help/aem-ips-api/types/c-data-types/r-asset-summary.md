---
title: 资产摘要
description: 包含有关资产的汇总信息的元数据搜索结果。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 10%

---

# [!DNL AssetSummary]{#assetsummary}

包含有关资产的汇总信息的元数据搜索结果。

语法

## 参数 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 资产句柄。 |
| 类型 | `xsd:string` | 资源类型。 “资产类型”常量定义可能的值。 可选. |
| 名称 | `xsd:string` | 资源名称。 可选. |
| 文件夹 | `xsd:string` | 包含资产的文件夹。 |
| 文件名 | `xsd:string` | 资源的文件名。 |
| 已创建 | `xsd:dateTime` | 资源创建日期。 |
| createUser | `xsd:string` | 创建资源的用户。 |
| lastModified | `xsd:dateTime` | 上次更新资产的日期。 |
| lastModifyUser | `xsd:string` | 上次修改资产的用户。 |
| metadataArray | `types:MetadataArray` | 与资源关联的元数据值数组。 |
| 分数 | `xsd:double` | 定义存在相似性搜索时的精度（0 =无匹配项，1 =完全匹配）。 |
| scoredetail | `xsd:string` | 它保存相似区域的详细信息，作为相似性搜索的结果。 |
