---
description: 由searchAssets返回的元数据字段。
solution: Experience Manager
title: 元数据
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
TQID: 'https://experienceleague.adobe.com/Cdg9mW2P4YXWlpTiP9ue6cXlFjCByFiw74iJl-sCYNk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 13%

---

# [!DNL Metadata]{#metadata}

由searchAssets返回的元数据字段。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 名称 | `xsd:string` | 元数据名称。 |
| 价值 | `xsd:string` | 元数据值。 |
| boolVal | `xsd:boolean` | 布尔元数据值（仅适用于布尔类型字段）。 |
| longVal | `xsd:long` | 长元数据值（仅适用于int类型的字段）。 |
| doubleVal | `xsd:double` | 双精度元数据值（仅适用于浮点类型字段）。 |
| 日期值 | `xsd:dateTime` | 日期元数据值（仅适用于日期类型字段）。 |

