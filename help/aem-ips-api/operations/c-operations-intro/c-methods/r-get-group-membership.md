---
description: 返回用户组成员。
seo-description: 返回用户组成员。
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
topic: Scene7 Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getGroupMembership{#getgroupmembership}

返回用户组成员。

语法

## 授权用户类型 {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2e92f850254e46e48403acaa215341a5}

**输入(getGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | 否 | 用户的句柄。 |
| ` *`companyHandle`*` | `xsd:string` | 否 | 公司的把手。 |

**输出(getGroupMembershipReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | 是 | 组数组。 |

## 示例 {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

此代码示例返回组的所有成员。 由于公司和用户句柄是可选的，因此该操作可以返回所有组的所有成员。

**请求**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**响应**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

