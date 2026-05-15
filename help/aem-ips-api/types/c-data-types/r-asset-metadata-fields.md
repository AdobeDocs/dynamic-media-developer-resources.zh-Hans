---
title: AssetMetadataField
description: 返回指定资源类型的元数据字段定义。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
TQID: 'https://experienceleague.adobe.com/U9JVe27HBTMtlBXmwDnkVAOaVfsBspa5r5fvnQl-h58'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 47
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

返回指定资源类型的元数据字段定义。

语法

## 参数 {#section-5ad771540c5f40c187b35e34aac19305}

| 名称 | 类型 | 说明 |
|---|---|---|
| 资产类型 | `xsd:string` | 与字段定义关联的资源类型（有关值，请参阅“资源类型”）。 |
| fieldArray | `types:MetadataFieldArray` | 与`assetType`中指定的资源类型关联的元数据字段定义数组。 |
