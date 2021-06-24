---
description: 当经过身份验证的用户没有足够的权限完成任务时引发。
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 25%

---

# authorizationFault{#authorizationfault}

当经过身份验证的用户没有足够的权限完成任务时引发。

语法

## 故障类型 {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | 故障 |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 20002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 20003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 20004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 20005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 20006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 20007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 20008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 20009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## 故障字段 {#section-4e3e41f41fea402a9ae314bfd05f663e}

| 名称 | 类型 | 说明 |
|---|---|---|
| `code` | `xsd:int` | 故障ID |
| `reason` | `xsd:string` | 描述故障的信息性消息。 |
