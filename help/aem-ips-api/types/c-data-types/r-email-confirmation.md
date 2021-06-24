---
description: 响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# EmailConfirmation{#emailconfirmation}

响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。

语法

## 参数 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | 如果为true，则包括用户的Web服务用户帐户，该帐户是指定用于从Dynamic Media CDN接收电子邮件确认的电子邮件列表。 |
| `*`ccOthersArray`*` | `types:EmailArray` | 一组电子邮件地址（最多5个），指定用于从Dynamic Media CDN接收确认通知。 |
