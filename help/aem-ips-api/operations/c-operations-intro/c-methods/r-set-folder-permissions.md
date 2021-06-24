---
description: 设置文件夹权限。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 14%

---

# setFolderPermissions{#setfolderpermissions}

设置文件夹权限。

语法

## 授权用户类型 {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-2a41135054954396b40f1228f2e63b42}

**输入(setFolderPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司负责人。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 文件夹句柄。 |
| `*`setChildren`*` | `xsd:boolean` | 是 | 设置属于该文件夹的子项的权限。 |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | 是 | 权限阵列。 |

**输出(setFolderPermissionsReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-01730da4be874553ab44e3241cdf6357}

此代码示例指定了公司句柄、文件夹句柄以及包含文件夹详细信息的权限数组。 它对父文件夹的子文件夹应用相同的权限。

**请求**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**响应**

无。
