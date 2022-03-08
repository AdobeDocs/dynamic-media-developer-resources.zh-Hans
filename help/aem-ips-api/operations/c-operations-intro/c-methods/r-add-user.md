---
description: 创建用户帐户并将该帐户添加到一个或多个公司。
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 13%

---

# addUser{#adduser}

创建用户帐户并将该帐户添加到一个或多个公司。

将用户添加到多个公司时，请按公司在中处理的公司来指定这些公司 `companyHandleArray`. 此操作会将句柄返回给您刚才添加的用户。

## 授权用户类型 {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-40390a512e314b8d80ecffbb7729f6fb}

**输入(addUserParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| firstName | `xsd:string` | 是 | 用户的名字。 |
| lastName | `xsd:string` | 是 | 用户的姓氏。 |
| 电子邮件 | `xsd:string` | 是 | 用户的电子邮件地址。 |
| defaultRole | `xsd:string` | 是 | 设置用户在其所属的每个公司中的角色。 但请注意， `IpsAdmin` 角色会覆盖其他按公司设置。 |
| 密码 | `xsd:string` | 是 | 设置用户的密码 |
| passwordExpires | `xsd:dateTime` | 否 | 设置密码过期期限。 在传入请求时提供时区。 时区将调整为“中央时间”。 |
| isValid | `xsd:boolean` | 是 | 确定用户是否有效。 |
| membersingArray | `xsd:CompanyMembershipUpdateArray` | 是 | 公司句柄数组。 |

**输出(addUserParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 是 | 用户的句柄。 |

## 示例 {#section-2547cef622734b71919eef849960b5cb}

IPS API会返回一个用户句柄元素，用于指定新用户。

**请求**

```java
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**响应**

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
