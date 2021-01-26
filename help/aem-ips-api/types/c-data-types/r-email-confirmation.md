---
description: 响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。
solution: Experience Manager
title: 电子邮件确认
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# EmailConfirmation{#emailconfirmation}

响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。

语法

## 参数 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | 如果为true，则包括用户的Web服务用户帐户，该帐户是指定从Dynamic MediaCDN接收电子邮件确认的电子邮件列表。 |
| `*`ccOthersArray`*` | `types:EmailArray` | 指定从Dynamic MediaCDN接收确认通知的一组电子邮件地址（最大5个）。 |

