---
description: 系统中资源和类型的用户。
solution: Experience Manager
title: 用户
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# 用户{#user}

系统中资源和类型的用户。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | 用户句柄。 |
| `*`firstName`*` | `xsd:string` | 用户名。 |
| `*`lastName`*` | `xsd:string` | 用户名。 |
| `*`电子邮件`*` | `xsd:string` | 电子邮件地址。 |
| `*`defaultRole`*` | `xsd:string` | 设置用户在其所属的每个公司中的角色。 但是，用户角色`IpsAmin`会覆盖其他用户角色。 |
| `*`isValid`*` | `xsd:boolean` | 确定用户是否有效。 |
| `*`passwordExpires`*` | `xsd:dateTime` | 设置密码过期日期。 |
