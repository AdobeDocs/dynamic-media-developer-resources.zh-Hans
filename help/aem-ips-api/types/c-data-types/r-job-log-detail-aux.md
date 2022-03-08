---
description: 包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告和与当前处理的资产关联的其他详细信息。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# JobLogDetailAux{#joblogdetailaux}

包含与主作业日志消息(JobDetail)关联的补充消息。 包括警告和与当前处理的资产关联的其他详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| logMessage | `xsd:string` | 辅助信息。 |
| logType | `xsd:string` | 日志类型： `IPSJobLog.gcUploadWarning` 或 `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | 辅助作业日志创建日期。 |
