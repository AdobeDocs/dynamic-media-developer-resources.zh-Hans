---
description: 设置用户属性（例如，名称、电子邮件、角色等）。
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
TQID: 'https://experienceleague.adobe.com/JzJv4nEeWfbY-Wp-qkEq883dlTqaRm9Fc-UvDa70dOg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 14%

---

# setUserInfo{#setuserinfo}

设置用户属性（例如，名称、电子邮件、角色等）。

语法

## 授权用户类型 {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-71b457921fe74acb862a1e112e550211}

**输入(setUserInfoParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 用户句柄。 |
| 名字 | `xsd:string` | 是 | 名字。 |
| 姓氏 | `xsd:string` | 是 | 姓氏。 |
| 电子邮件 | `xsd:string` | 是 | 用户电子邮件。 |
| defaultrole | `xsd:string` | 是 | 设置用户在其所属的每个公司中的角色。 但请注意，`IpsAdmin`角色将覆盖其他按公司划分的设置。 |
| passwordExpires | `xsd:dateTime` | 否 | 设置的密码过期日期。 |
| isValid | `xsd:boolean` | 是 | 确定用户是否为有效的IPS用户。 |
| membershipArray | `types:CompanyMembershipUpdateArray` | 是 | 公司句柄数组。 |

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
