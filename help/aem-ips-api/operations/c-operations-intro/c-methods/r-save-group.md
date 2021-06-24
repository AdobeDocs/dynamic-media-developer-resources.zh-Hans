---
description: 创建或编辑群组。
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 21%

---

# saveGroup{#savegroup}

创建或编辑群组。

语法

## 授权用户类型 {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-743610e98dd5494baffcbad6401038eb}

**输入(saveGroupParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要保存的组的公司的句柄。 |
| `*`groupHandle`*` | `xsd:string` | 否 | 组的句柄。 |
| `*`name`*` | `xsd:string` | 是 | 群组名称. |
| `*`isSystemDefined`*` | `xsd:boolean` | 是 | `false` 为默认值。 |

**输出(saveGroupReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 是 | 组句柄。 |

## 示例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

此代码示例会创建属于特定公司的组。 如果组已存在，则会使用您指定的参数值进行保存。

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
