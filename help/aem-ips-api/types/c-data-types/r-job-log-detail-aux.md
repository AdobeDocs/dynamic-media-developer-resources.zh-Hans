---
description: 包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告以及与当前处理的资产关联的其他详细信息。
seo-description: 包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告以及与当前处理的资产关联的其他详细信息。
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Scene7 Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告以及与当前处理的资产关联的其他详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | 辅助信息。 |
| ` *`logType`*` | `xsd:string` | 日志类型：`IPSJobLog.gcUploadWarning`或`IPSJobLog.gcUploadError`。 |
| ` *`dateCreated`*` | `xsd:dateTime` | 辅助作业日志创建日期。 |

