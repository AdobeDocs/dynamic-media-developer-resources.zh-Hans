---
description: 当用户无法通过身份验证时引发。
solution: Experience Manager
title: authenticationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 21%

---


# authenticationFault{#authenticationfault}

当用户无法通过身份验证时引发。

语法

## 故障类型{#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 故障 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## 故障字段{#section-1fe84846a7154b03ab49552810ee9ac3}

| 名称 | 类型 | 说明 |
|---|---|---|
| `code` | `xsd:int` | 错误ID |
| `reason` | `xsd:string` | 描述错误的信息。 |
