---
description: 向指定收件人发送电子邮件以响应cdnCacheInvalidation操作。
solution: Experience Manager
title: 电子邮件确认
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

向指定收件人发送电子邮件以响应cdnCacheInvalidation操作。

语法

## 参数 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名称 | 类型 | 说明 |
|---|---|---|
| 创作者 | `xsd:boolean` | 如果为true，则包括用户的Web服务用户帐户，该帐户是指定从Dynamic Media CDN接收电子邮件确认的电子邮件列表。 |
| ccOthersArray | `types:EmailArray` | 用于从Dynamic Media CDN接收确认通知的电子邮件地址数组（最多5个）。 |
