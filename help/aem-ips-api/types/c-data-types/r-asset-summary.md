---
title: 资产摘要
description: 包含有关资产的汇总信息的元数据搜索结果。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
TQID: 'https://experienceleague.adobe.com/RHT8NJiS0pGKUcrYGBsSI1vewvRGUCZmsPYP6Pb0OBs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 125
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
| 分數 | `xsd:double` | 定义存在相似性搜索时的精度（0 =无匹配项，1 =完全匹配）。 |
| scoredetail | `xsd:string` | 它保存相似区域的详细信息，作为相似性搜索的结果。 |

