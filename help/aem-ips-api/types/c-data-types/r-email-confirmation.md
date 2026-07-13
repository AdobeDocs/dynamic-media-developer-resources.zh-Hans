---
description: 向指定收件人发送电子邮件以响应cdnCacheInvalidation操作。
solution: Experience Manager
title: 电子邮件确认
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

向指定收件人发送电子邮件以响应cdnCacheInvalidation操作。

语法

## 参数 {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| 名称 | 类型 | 说明 |
|---|---|---|
| 创作者 | `xsd:boolean` | 如果为true，则包括用户的Web服务用户帐户，该帐户是指定从Dynamic Media CDN接收电子邮件确认的电子邮件列表。 |
| ccOthersArray | `types:EmailArray` | 指定用于从Dynamic Media CDN接收确认通知的电子邮件地址数组（最多5个）。 |

