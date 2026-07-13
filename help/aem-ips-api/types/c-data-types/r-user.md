---
description: 系统中资源和类型的用户。
solution: Experience Manager
title: 用户
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 9%

---

# [!DNL User]{#user}

系统中资源和类型的用户。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| userHandle | `xsd:string` | 用户句柄。 |
| 名字 | `xsd:string` | 用户名字。 |
| 姓氏 | `xsd:string` | 用户姓氏。 |
| 电子邮件 | `xsd:string` | 电子邮件地址。 |
| defaultrole | `xsd:string` | 设置用户在其所属的每个公司中的角色。 但是，用户角色`IpsAmin`将覆盖其他用户角色。 |
| isValid | `xsd:boolean` | 确定用户是否有效。 |
| passwordExpires | `xsd:dateTime` | 设置密码到期日期。 |

