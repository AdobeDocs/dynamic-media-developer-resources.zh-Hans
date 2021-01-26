---
description: 获取属于特定公司和组的用户。
seo-description: 获取属于特定公司和组的用户。
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Dynamic Media Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 16%

---


# getGroupMembers{#getgroupmembers}

获取属于特定公司和组的用户。

语法

## 授权用户类型{#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b798b06354c946abbb90fa72cc9c67fd}

**输入(getGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`groupHandle`*` | `xsd:string` |  | 组的句柄。 |

**输出(getGroupMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | 是 | 一组用户句柄。 |

## 示例 {#section-aaa340dba6b64cce9bcd8303cf999166}

此代码示例返回包含属于特定组的所有用户的用户句柄数组。

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

