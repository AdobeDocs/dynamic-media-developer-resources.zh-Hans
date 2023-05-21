---
description: 傳回公司控制代碼所指定之公司的使用者。
solution: Experience Manager
title: getCompanyMember
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 17%

---

# getCompanyMember{#getcompanymembers}

傳回公司控制代碼所指定之公司的使用者。

语法

## 授權的使用者型別 {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-5602e4d6f2214e398e6a804e61f1a088}

**輸入(getCompanyMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 您要取得其成員之公司的控制代碼。 |
| includeInvalid | `xsd:boolean` | 是 | 包含無效公司。 |

**輸出(getCompanyMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | 是 | 使用者會籍陣列。 |

## 示例 {#section-39d8cf3653fd4fe8b842caabac9dedfc}

此程式碼範例會傳回使用者陣列中公司的所有成員。 回應因簡短而遭截斷。

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
