---
description: 系统中资源和类型的用户。
solution: Experience Manager
title: 用户
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
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
| defaultrole | `xsd:string` | 设置用户在其所属的每个公司中的角色。 但是，用户角色 `IpsAmin` 覆盖其他用户角色。 |
| isValid | `xsd:boolean` | 确定用户是否有效。 |
| passwordExpires | `xsd:dateTime` | 设置密码到期日期。 |
