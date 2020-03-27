---
description: 响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。
seo-description: 响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。
seo-title: 电子邮件确认
solution: Experience Manager
title: 电子邮件确认
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 电子邮件确认{#emailconfirmation}

响应cdnCacheInvalidation操作，向指定收件人发送电子邮件。

语法

## 参数 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | 如果为true，则包括用户的Web服务用户帐户，该帐户是指定从Scene7 CDN接收电子邮件确认的电子邮件列表。 |
| ` *`ccOthersArray`*` | `types:EmailArray` | 一组电子邮件地址（最大5个），指定用于从Scene7 CDN接收确认通知。 |

