---
description: 返回由公司句柄指定的公司的用户。
seo-description: 返回由公司句柄指定的公司的用户。
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 14%

---


# getCompanyMembers{#getcompanymembers}

返回由公司句柄指定的公司的用户。

语法

## 授权用户类型{#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-5602e4d6f2214e398e6a804e61f1a088}

**输入(getCompanyMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要获取其成员的公司的句柄。 |
| `*`includeInvalid`*` | `xsd:boolean` | 是 | 包含无效公司。 |

**输出(getCompanyMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | 是 | 用户成员数组。 |

## 示例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

此代码示例返回用户数组中公司的所有成员。 响应被截断，以致简短。

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

