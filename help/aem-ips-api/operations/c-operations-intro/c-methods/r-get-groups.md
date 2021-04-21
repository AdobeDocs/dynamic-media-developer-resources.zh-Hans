---
description: 返回公司组。
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 20%

---


# getGroups{#getgroups}

返回公司组。

语法

## 授权用户类型{#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-0e06195f23dd4c69922df210f566dd18}

**输入(getGroupsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的手柄。 |

**输出(getGroupsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | 是 | 组数组。 |

## 示例 {#section-ed0708f611574354bf0c6ea83912b531}

此代码返回一个数组，其中包含属于特定公司的所有组以及每个组的特定信息。

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

