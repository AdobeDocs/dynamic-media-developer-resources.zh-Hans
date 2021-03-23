---
description: 创建或编辑用户组。
seo-description: 创建或编辑用户组。
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 20%

---


# saveGroup{#savegroup}

创建或编辑用户组。

语法

## 授权用户类型{#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-743610e98dd5494baffcbad6401038eb}

**输入(saveGroupParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要保存的组的公司的句柄。 |
| `*`groupHandle`*` | `xsd:string` | 否 | 组的句柄。 |
| `*`name`*` | `xsd:string` | 是 | 群组名称. |
| `*`isSystemDefined`*` | `xsd:boolean` | 是 | `false` 。 |

**输出(saveGroupReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 是 | 组句柄。 |

## 示例 {#section-26eee227ff1f4edabb7fa1240b4d9999}

此代码示例创建属于特定公司的组。 如果组已存在，则会使用您指定的参数值保存该组。

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

