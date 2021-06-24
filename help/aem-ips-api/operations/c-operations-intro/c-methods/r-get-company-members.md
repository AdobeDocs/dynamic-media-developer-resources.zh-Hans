---
description: 返回由公司句柄指定的公司的用户。
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 17%

---

# getCompanyMembers{#getcompanymembers}

返回由公司句柄指定的公司的用户。

语法

## 授权用户类型 {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-5602e4d6f2214e398e6a804e61f1a088}

**输入(getCompanyMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要获取其成员的公司的句柄。 |
| `*`includeInvalid`*` | `xsd:boolean` | 是 | 包括无效公司。 |

**Output(getCompanyMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | 是 | 用户成员资格数组。 |

## 示例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

此代码示例可返回用户数组中公司的所有成员。 响应已被截断，以便简短。

**请求**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**响应**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```
