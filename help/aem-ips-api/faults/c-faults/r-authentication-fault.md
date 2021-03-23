---
description: 当用户无法通过身份验证时引发。
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---


# authenticationFault{#authenticationfault}

当用户无法通过身份验证时引发。

语法

## 故障类型{#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 错误 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## 故障字段{#section-1fe84846a7154b03ab49552810ee9ac3}

| 名称 | 类型 | 说明 |
|---|---|---|
| `code` | `xsd:int` | 错误ID |
| `reason` | `xsd:string` | 描述错误的信息。 |
