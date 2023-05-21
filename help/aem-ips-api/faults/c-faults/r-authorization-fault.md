---
description: 當已驗證的使用者沒有足夠的許可權完成任務時擲回。
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 27%

---

# authorizationFault{#authorizationfault}

當已驗證的使用者沒有足夠的許可權完成任務時擲回。

语法

## 錯誤型別 {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | 錯誤 |
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

## 錯誤欄位 {#section-4e3e41f41fea402a9ae314bfd05f663e}

| 名称 | 类型 | 说明 |
|---|---|---|
| `code` | `xsd:int` | 錯誤ID |
| `reason` | `xsd:string` | 說明錯誤的資訊性訊息。 |
