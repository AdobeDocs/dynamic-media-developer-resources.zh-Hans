---
description: 設定使用者屬性（例如名稱、電子郵件、角色等）
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 17%

---

# setUserInfo{#setuserinfo}

設定使用者屬性（例如名稱、電子郵件、角色等）

语法

## 授權的使用者型別 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-71b457921fe74acb862a1e112e550211}

**輸入(setUserInfoParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 使用者控制代碼。 |
| 名字 | `xsd:string` | 是 | 名字。 |
| 姓氏 | `xsd:string` | 是 | 姓氏。 |
| 电子邮件 | `xsd:string` | 是 | 使用者電子郵件。 |
| 預設角色 | `xsd:string` | 是 | 設定使用者在其所屬每個公司中的角色。 但是請注意 `IpsAdmin` 角色會覆寫其他每個公司的設定。 |
| passwordExpires | `xsd:dateTime` | 否 | 設定的密碼到期日。 |
| isValid | `xsd:boolean` | 是 | 判斷使用者是否為有效的IPS使用者。 |
| memberlationarray | `types:CompanyMembershipUpdateArray` | 是 | 公司控點的陣列。 |

**輸出(setUserInfoReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-272c103076fb4de0a53729e2f6bfb895}

**请求**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**响应**

无。
