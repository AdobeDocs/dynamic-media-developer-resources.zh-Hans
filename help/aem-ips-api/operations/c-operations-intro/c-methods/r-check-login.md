---
description: 檢查具有特定公司（由控制代碼識別）、電子郵件地址和密碼的使用者是否可以登入。
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 13%

---

# checkLogin{#checklogin}

檢查具有特定公司（由控制代碼識別）、電子郵件地址和密碼的使用者是否可以登入。

>[!NOTE]
>
>如果省略公司控制代碼，此方法會檢查預設使用者的登入。

## 授權的使用者型別 {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-1ad4c0b4803b4388aedd655030676cb3}

**輸入(checkLoginParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 包含使用者的公司的控制代碼。 |
| 电子邮件 | `xsd:string` | 是 | 使用者的電子郵件地址。 |
| 密码 | `xsd:string` | 是 | 使用者的密碼。 |

**輸出(checkLoginParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 状态 | `xsd:string` | 是 | 使用者的登入狀態。 |

## 示例 {#section-23f90100a9d94bc7b4045634cccd1b98}

此程式碼範例使用公司控制代碼引數、電子郵件地址和密碼來判斷使用者是否可以登入IPS。 若使用者 *可以* 登入，此方法會傳回字串， `ValidLogin`. 若使用者 *無法* 登入，此方法會傳回字串， `InvalidLogin`.

**请求**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**响应**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```
