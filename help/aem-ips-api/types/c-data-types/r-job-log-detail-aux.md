---
description: 包含與主要工作記錄檔訊息(JobDetail)相關聯的補充訊息。 包含警告和與目前處理之資產相關聯的其他詳細資訊。
solution: Experience Manager
title: 工作記錄詳細資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

包含與主要工作記錄檔訊息(JobDetail)相關聯的補充訊息。 包含警告和與目前處理之資產相關聯的其他詳細資訊。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| logMessage | `xsd:string` | 輔助訊息。 |
| logType | `xsd:string` | 記錄型別： `IPSJobLog.gcUploadWarning` 或 `IPSJobLog.gcUploadError`. |
| dateCreate | `xsd:dateTime` | 輔助工作記錄檔建立日期。 |
