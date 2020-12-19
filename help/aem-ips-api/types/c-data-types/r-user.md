---
description: 系统中资源和类型的用户。
seo-description: 系统中资源和类型的用户。
seo-title: 用户
solution: Experience Manager
title: 用户
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 10%

---


# 用户{#user}

系统中资源和类型的用户。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 用户句柄。 |
| ` *`firstName`*` | `xsd:string` | 用户名。 |
| ` *`lastName`*` | `xsd:string` | 用户名。 |
| ` *`电子邮件`*` | `xsd:string` | 电子邮件地址。 |
| ` *`defaultRole`*` | `xsd:string` | 在用户所属的每个公司中设置用户的角色。 但是，用户角色`IpsAmin`将覆盖其他用户角色。 |
| ` *`isValid`*` | `xsd:boolean` | 确定用户是否有效。 |
| ` *`passwordExpires`*` | `xsd:dateTime` | 设置密码过期日期。 |

