---
description: 管理依群組存取、修改、建立或刪除資產的許可權。
solution: Experience Manager
title: 許可權
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---

# [!DNL Permission]{#permission}

管理依群組存取、修改、建立或刪除資產的許可權。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| groupHandle | `xsd:string` | 群組控制代碼。 |
| groupName | `xsd:string` | 群组名称. |
| permissiontype | `xsd:string` | 選擇許可權型別。 |
| isAllowed | `xsd:boolean` | 決定是否允許許可權。 |
| isOverride | `xsd:boolean` | 決定許可權是否覆寫其他許可權。 |
