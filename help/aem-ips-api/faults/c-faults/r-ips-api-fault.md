---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
topic: Dynamic Media Image Production System API
uuid: 010814a8-1d29-4b02-8449-cb26e4335e07
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '25'
ht-degree: 36%

---


# ipsApiFault{#ipsapifault}

语法

## 故障类型{#section-425697675cac4b2ab5c48bd463956401}

| ID | 故障 |
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

