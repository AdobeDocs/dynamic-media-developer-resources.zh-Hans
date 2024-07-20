---
description: 由searchAssets返回的元数据字段。
solution: Experience Manager
title: 元数据
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

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
