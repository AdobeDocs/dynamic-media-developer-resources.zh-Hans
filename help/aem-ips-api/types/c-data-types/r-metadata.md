---
description: searchAssets返回的元数据字段。
solution: Experience Manager
title: 元数据
feature: Dynamic Media Classic，SDK/API，元数据
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 12%

---


# 元数据{#metadata}

searchAssets返回的元数据字段。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 元数据名称。 |
| `*`值`*` | `xsd:string` | 元数据值。 |
| `*`boolVal`*` | `xsd:boolean` | Boolean元数据值（仅用于Boolean类型字段）。 |
| `*`longVal`*` | `xsd:long` | 长元数据值（仅适用于int-typed字段）。 |
| `*`doubleVal`*` | `xsd:double` | 多次元数据值（仅适用于浮动类型字段）。 |
| `*`dateVal`*` | `xsd:dateTime` | 日期元数据值（仅适用于日期类型字段）。 |

