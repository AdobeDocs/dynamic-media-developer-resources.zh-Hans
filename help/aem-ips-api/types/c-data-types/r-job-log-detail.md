---
description: 作业日志信息。
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# JobLogDetail{#joblogdetail}

作业日志信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 作业日志中的消息。 |
| `*`logType`*` | `xsd:string` | 作业日志文件类型。 |
| `*`assetName`*` | `xsd:string` | 作业日志中资产的名称（可选）。 |
| `*`assetType`*` | `xsd:string` | 资产类型的选择。 |
| `*`assetHandle`*` | `xsd:string` | 作业日志中引用的资产句柄。 |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | 提供上述五个作业日志类型之外的其他详细作业日志信息。 |

