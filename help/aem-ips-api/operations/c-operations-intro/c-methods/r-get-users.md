---
description: 获取由公司、组和用户角色句柄指定的用户数组。 此操作允许您对返回的用户进行排序，并按字符进行过滤。
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 10%

---

# getUsers{#getusers}

获取由公司、组和用户角色句柄指定的用户数组。 此操作允许您对返回的用户进行排序，并按字符进行过滤。

## 授权用户类型 {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | 否 | 包括或排除不活动的用户。 非IPS管理员用户必须是至少一家公司的活动成员，才能获得授权进行任何API调用。 如果用户没有有效的公司成员资格，则会返回授权错误。 |
| `*`includeInvalid`*` | `xsd:boolean` | 否 | 允许您包含/排除无效用户。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 否 | 按公司筛选结果。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 否 | 按组筛选结果。 |
| `*`userRoleArray`*` | `types:StringArray` | 否 | 按用户角色筛选结果。 |
| `*`charFilterField`*` | `xsd:string` | 否 | 按字段的字符串前缀筛选结果(请参阅[!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | 否 | 按特定字符过滤结果。 |
| `*`sortBy`*` | `xsd:string` | 否 | 用户排序字段的选项。 |
| `*`recordsPerPage`*` | `xsd:int` | 否 | 返回每页指定的记录数。 |
| `*`resultsPage`*` | `xsd:int` | 否 | 结果页面。 |

**Output(getUsersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | 是 | 一组用户。 |

## 示例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

此代码示例为多个可选参数返回用户数组。 用户角色、用户字符过滤器字段和用户排序字段通过使用特定的字符串常量来确定。

**请求**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**响应**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
