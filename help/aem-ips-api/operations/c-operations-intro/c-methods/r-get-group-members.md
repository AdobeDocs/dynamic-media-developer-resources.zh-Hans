---
description: 取得屬於特定公司和群組的使用者。
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---

# getGroupMembers{#getgroupmembers}

取得屬於特定公司和群組的使用者。

语法

## 授權的使用者型別 {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b798b06354c946abbb90fa72cc9c67fd}

**輸入(getGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |
| groupHandle | `xsd:string` |  | 群組的控制代碼。 |

**輸出(getGroupMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | 是 | 使用者控制代碼陣列。 |

## 示例 {#section-aaa340dba6b64cce9bcd8303cf999166}

此程式碼範例會傳回包含屬於特定群組之所有使用者的使用者控制代碼陣列。

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
