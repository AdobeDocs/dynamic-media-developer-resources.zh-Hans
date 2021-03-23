---
description: 检查具有特定公司（通过句柄标识）、电子邮件地址和密码的用户是否可以登录。
seo-description: 检查具有特定公司（通过句柄标识）、电子邮件地址和密码的用户是否可以登录。
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 11%

---


# checkLogin{#checklogin}

检查具有特定公司（通过句柄标识）、电子邮件地址和密码的用户是否可以登录。

>[!NOTE]
>
>如果省略公司句柄，此方法将检查默认用户的登录名。

## 授权用户类型{#section-df8b26b550854f899948276adaca083a}

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

**Input(checkLoginParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 包含用户的公司的句柄。 |
| `*`电子邮件`*` | `xsd:string` | 是 | 用户的电子邮件地址。 |
| `*`密码`*` | `xsd:string` | 是 | 用户的密码。 |

**输出(checkLoginParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`状态`*` | `xsd:string` | 是 | 用户的登录状态。 |

## 示例 {#section-23f90100a9d94bc7b4045634cccd1b98}

此示例代码使用公司句柄参数、电子邮件地址和密码来确定用户是否可以登录IPS。 如果用户&#x200B;*可以*&#x200B;登录，则此方法返回字符串`ValidLogin`。 如果用户&#x200B;*无法*&#x200B;登录，则此方法返回字符串`InvalidLogin`。

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

