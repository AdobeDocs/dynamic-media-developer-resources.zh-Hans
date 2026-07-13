---
description: 检查具有特定公司（由句柄标识）、电子邮件地址和密码的用户是否可以登录。
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
TQID: 'https://experienceleague.adobe.com/5o2geLVIOZLg7tmKrHueWkzjf4EhXedAJ5qvWxTzjB0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 11%

---

# checkLogin{#checklogin}

检查具有特定公司（由句柄标识）、电子邮件地址和密码的用户是否可以登录。

>[!NOTE]
>
>如果省略公司句柄，此方法将检查默认用户的登录名。

## 授权用户类型 {#section-df8b26b550854f899948276adaca083a}

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

**输入(checkLoginParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 包含用户的公司的句柄。 |
| 电子邮件 | `xsd:string` | 是 | 用户的电子邮件地址。 |
| 密码 | `xsd:string` | 是 | 用户的密码。 |

**输出(checkLoginParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 状态 | `xsd:string` | 是 | 用户的登录状态。 |

## 示例 {#section-23f90100a9d94bc7b4045634cccd1b98}

此示例代码使用公司句柄参数、电子邮件地址和密码来确定用户是否可以登录IPS。 如果用户&#x200B;*可以*&#x200B;登录，此方法将返回字符串`ValidLogin`。 如果用户&#x200B;*无法*&#x200B;登录，此方法将返回字符串`InvalidLogin`。

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

