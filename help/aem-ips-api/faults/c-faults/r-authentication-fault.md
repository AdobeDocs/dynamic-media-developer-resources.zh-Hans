---
description: 当用户无法进行身份验证时引发。
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 19%

---

# authenticationFault{#authenticationfault}

当用户无法进行身份验证时引发。

语法

## 故障类型 {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 故障 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## 故障字段 {#section-1fe84846a7154b03ab49552810ee9ac3}

| 名称 | 类型 | 说明 |
|---|---|---|
| `code` | `xsd:int` | 故障ID |
| `reason` | `xsd:string` | 描述故障的信息性消息。 |
