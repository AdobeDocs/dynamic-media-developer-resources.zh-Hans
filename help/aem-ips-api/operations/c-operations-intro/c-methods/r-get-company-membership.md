---
description: 获取公司数组中用户的成员资格。
solution: Experience Manager
title: getCompanyMembersing
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

---

# getCompanyMembersing{#getcompanymembership}

获取公司数组中用户的成员资格。

语法

## 授权用户类型 {#section-f8bba547e1f648648be99dc48fd72b5d}

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

**输入(getCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要获取其成员资格的用户的句柄。 |

**Output(getCompanyMembershipReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`membersingArray`*` | `types:CompanyMembershipArray` | 是 | 公司成员资格数组。 |

## 示例 {#section-e4958d104ea344a4a79f57d07b46eba7}

此代码示例获取用户句柄并获取数组中所有用户的公司成员资格。 响应已被截断，以便简短。

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
