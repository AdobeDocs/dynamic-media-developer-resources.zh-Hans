---
description: 获取公司数组中用户的成员关系。
seo-description: 获取公司数组中用户的成员关系。
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 15%

---


# getCompanyMembership{#getcompanymembership}

获取公司数组中用户的成员关系。

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
| `*`userHandle`*` | `xsd:string` | 否 | 要获取其成员身份的用户的句柄。 |

**输出(getCompanyMembershipReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`membershArray`*` | `types:CompanyMembershipArray` | 是 | 公司成员关系数组。 |

## 示例 {#section-e4958d104ea344a4a79f57d07b46eba7}

此代码示例获取用户句柄，并获取数组中用户的所有公司成员关系。 响应被截断，以致简短。

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

