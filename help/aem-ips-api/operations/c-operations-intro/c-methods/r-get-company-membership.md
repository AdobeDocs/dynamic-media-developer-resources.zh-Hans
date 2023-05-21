---
description: 取得使用者在公司陣列中的成員資格。
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---

# getCompanyMembership{#getcompanymembership}

取得使用者在公司陣列中的成員資格。

语法

## 授權的使用者型別 {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-8745c360c3e1400a88e9bdb26bcb93de}

**輸入(getCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 您要取得其成員資格之使用者的控制代碼。 |

**輸出(getCompanyMembershipReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| memberlationarray | `types:CompanyMembershipArray` | 是 | 公司成員資格陣列。 |

## 示例 {#section-e4958d104ea344a4a79f57d07b46eba7}

此程式碼範例取得使用者控制代碼，並在陣列中取得使用者的所有公司成員資格。 回應因簡短而遭截斷。

**请求**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**响应**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
