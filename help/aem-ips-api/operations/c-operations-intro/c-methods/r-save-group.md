---
description: 创建或编辑组。
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 18%

---

# saveGroup{#savegroup}

创建或编辑组。

语法

## 授权用户类型 {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-743610e98dd5494baffcbad6401038eb}

**输入(saveGroupParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要保存的组的公司的句柄。 |
| groupHandle | `xsd:string` | 否 | 组的句柄。 |
| 名称 | `xsd:string` | 是 | 组名称。 |
| isSystemDefined | `xsd:boolean` | 是 | `false`是默认的。 |

**输出(saveGroupReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| groupHandle | `xsd:string` | 是 | 组句柄。 |

## 示例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

此代码示例创建一个属于特定公司的组。 如果组已存在，则会使用您指定的参数值保存该组。

**请求**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**响应**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```
