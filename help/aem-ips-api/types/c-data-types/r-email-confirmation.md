---
description: 响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。
solution: Experience Manager
title: 电子邮件确认
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# EmailConfirmation{#emailconfirmation}

响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。

语法

## 参数 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | 如果为true，则包括用户的Web服务用户帐户，该帐户是指定从Dynamic Media CDN接收电子邮件确认的电子邮件列表。 |
| `*`ccOthersArray`*` | `types:EmailArray` | 一组电子邮件地址（最多5个），指定用于从Dynamic Media CDN接收确认通知。 |

