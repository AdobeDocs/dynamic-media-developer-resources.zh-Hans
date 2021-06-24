---
description: 获取属于特定公司和群组的用户。
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

---

# getGroupMembers{#getgroupmembers}

获取属于特定公司和群组的用户。

语法

## 授权用户类型 {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b798b06354c946abbb90fa72cc9c67fd}

**输入(getGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`groupHandle`*` | `xsd:string` |  | 组的句柄。 |

**Output(getGroupMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | 是 | 用户句柄数组。 |

## 示例 {#section-aaa340dba6b64cce9bcd8303cf999166}

此代码示例会返回一个用户句柄数组，其中包含属于某个特定组的所有用户。

**请求**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**响应**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```
