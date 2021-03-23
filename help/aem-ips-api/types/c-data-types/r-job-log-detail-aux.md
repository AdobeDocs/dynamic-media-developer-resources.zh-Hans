---
description: 包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告以及与当前处理的资产关联的其他详细信息。
seo-description: 包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告以及与当前处理的资产关联的其他详细信息。
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告以及与当前处理的资产关联的其他详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | 辅助信息。 |
| `*`logType`*` | `xsd:string` | 日志类型：`IPSJobLog.gcUploadWarning`或`IPSJobLog.gcUploadError`。 |
| `*`dateCreated`*` | `xsd:dateTime` | 辅助作业日志创建日期。 |

