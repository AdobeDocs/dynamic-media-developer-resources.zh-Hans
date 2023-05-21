---
description: 系統中資源和型別的使用者。
solution: Experience Manager
title: 用户
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---

# [!DNL User]{#user}

系統中資源和型別的使用者。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| userHandle | `xsd:string` | 使用者控制代碼。 |
| 名字 | `xsd:string` | 使用者名字。 |
| 姓氏 | `xsd:string` | 使用者姓氏。 |
| 电子邮件 | `xsd:string` | 電子郵件地址。 |
| 預設角色 | `xsd:string` | 設定使用者在其所屬每個公司中的角色。 但是，使用者角色 `IpsAmin` 覆寫其他使用者角色。 |
| isValid | `xsd:boolean` | 判斷使用者是否有效。 |
| passwordExpires | `xsd:dateTime` | 設定密碼到期日。 |
