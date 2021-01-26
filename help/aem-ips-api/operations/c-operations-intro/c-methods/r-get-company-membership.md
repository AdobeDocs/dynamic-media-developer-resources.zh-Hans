---
description: 获取公司数组中用户的成员资格。
seo-description: 获取公司数组中用户的成员资格。
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
topic: Dynamic Media Image Production System API
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 16%

---


# getCompanyMembership{#getcompanymembership}

获取公司数组中用户的成员资格。

语法

## 授权用户类型{#section-f8bba547e1f648648be99dc48fd72b5d}

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
| `*`userHandle`*` | `xsd:string` | 否 | 要获得其成员资格的用户的句柄。 |

**输出(getCompanyMembershipReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`membersArray`*` | `types:CompanyMembershipArray` | 是 | 公司成员资格的数组。 |

## 示例 {#section-e4958d104ea344a4a79f57d07b46eba7}

此代码示例采用用户句柄并获取数组中所有用户的公司成员关系。 响应被截断为简短。

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

