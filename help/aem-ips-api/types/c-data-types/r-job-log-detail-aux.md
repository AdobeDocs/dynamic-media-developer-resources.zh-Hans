---
description: 包含与主作业日志消息(JobDetail)关联的补充消息。 包括与当前已处理资源关联的警告和其他详细信息。
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
TQID: 'https://experienceleague.adobe.com/Hl3L69Hd6Hm8acRaPgFVQCfo8PffGCn5fNGxthmStFM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 64
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

