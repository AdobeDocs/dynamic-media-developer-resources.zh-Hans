---
description: 设置用户属性（例如名称、电子邮件、角色等）
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 16%

---


# setUserInfo{#setuserinfo}

设置用户属性（例如名称、电子邮件、角色等）

语法

## 授权用户类型{#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-71b457921fe74acb862a1e112e550211}

**Input(setUserInfoParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 用户句柄。 |
| `*`firstName`*` | `xsd:string` | 是 | 名字。 |
| `*`lastName`*` | `xsd:string` | 是 | 姓氏。 |
| `*`电子邮件`*` | `xsd:string` | 是 | 用户电子邮件。 |
| `*`defaultRole`*` | `xsd:string` | 是 | 在用户所属的每个公司中设置用户的角色。 但是，请注意，`IpsAdmin`角色将覆盖其他每公司设置。 |
| `*`passwordExpires`*` | `xsd:dateTime` | 否 | 设置密码过期日期。 |
| `*`isValid`*` | `xsd:boolean` | 是 | 确定用户是否为有效的IPS用户。 |
| `*`membershArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 一组公司手柄。 |

**输出(setUserInfoReturn)**

IPS API不返回此操作的响应。

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
