---
description: 设置文件夹权限。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
TQID: 'https://experienceleague.adobe.com/r-WGRjE263vPSVKsBieklQ79SASbDQOx9hp5IzS0-O0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 13%

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
| companyHandle | `xsd:string` | 是 | 公司句柄。 |
| folderHandle | `xsd:string` | 是 | 文件夹句柄。 |
| setchildren | `xsd:boolean` | 是 | 设置属于该文件夹的子项的权限。 |
| permissionArray | `types:PermissionUpdateArray` | 是 | 权限数组。 |

**输出(setFolderPermissionsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-01730da4be874553ab44e3241cdf6357}

此代码示例指定公司句柄、文件夹句柄和权限数组，其中包含有关文件夹的详细信息。 它会将相同的权限应用于父文件夹的子文件夹。

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
