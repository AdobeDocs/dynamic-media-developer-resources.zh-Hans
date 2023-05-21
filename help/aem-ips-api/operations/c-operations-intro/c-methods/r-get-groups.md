---
description: 傳回公司群組。
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 22%

---

# getGroups{#getgroups}

傳回公司群組。

语法

## 授權的使用者型別 {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-0e06195f23dd4c69922df210f566dd18}

**輸入(getGroupsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |

**輸出(getGroupsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| groupArray | `types:GroupArray` | 是 | 群組陣列。 |

## 示例 {#section-ed0708f611574354bf0c6ea83912b531}

此程式碼會傳回陣列，其中包含屬於特定公司的所有群組，以及每個群組的特定資訊。

**请求**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
