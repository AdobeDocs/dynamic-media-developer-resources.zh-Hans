---
description: 返回公司句柄指定的公司的用户。
solution: Experience Manager
title: getCompanyMember
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
TQID: 'https://experienceleague.adobe.com/QMJGqj7IEplTMdFFwVP3UReZAJsi25tHaaMewM30MSU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 15%

---

# getCompanyMember{#getcompanymembers}

返回公司句柄指定的公司的用户。

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
| companyHandle | `xsd:string` | 是 | 要获取其成员的公司的句柄。 |
| includeInvalid | `xsd:boolean` | 是 | 包含无效公司。 |

**输出(getCompanyMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | 是 | 用户成员资格数组。 |

## 示例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

此代码示例返回用户数组中公司的所有成员。 为简短起见，响应已截断。

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

