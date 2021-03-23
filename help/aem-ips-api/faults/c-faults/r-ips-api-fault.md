---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
uuid: 010814a8-1d29-4b02-8449-cb26e4335e07
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 28%

---


# ipsApiFault{#ipsapifault}

语法

## 故障类型{#section-425697675cac4b2ab5c48bd463956401}

| ID | 错误 |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## 故障字段{#section-37fe1aef1d5f4ca480071ca933aba826}

| 名称 | 类型 | 说明 |
|---|---|---|
| `code` | `xsd:int` | 错误ID |
| `reason` | `xsd:string` | 描述错误的信息。 |

