---
description: 包含与主作业日志消息(JobDetail)关联的补充消息。 包括与当前已处理资源关联的警告和其他详细信息。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

包含与主作业日志消息(JobDetail)关联的补充消息。 包括与当前已处理资源关联的警告和其他详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| logMessage | `xsd:string` | 辅助消息。 |
| logType | `xsd:string` | 日志类型： `IPSJobLog.gcUploadWarning`或`IPSJobLog.gcUploadError`。 |
| 创建日期 | `xsd:dateTime` | 辅助作业日志创建日期。 |
