---
description: 使用权限资产设置单个资产的权限。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 9%

---

# setAssetPermissions{#setassetpermissions}

使用权限资产设置单个资产的权限。

默认情况下，资产会继承其父文件夹的权限。 在资产上设置权限后，资产将不再继承其父资产的权限，除非您调用`removeAssetPermissions`。

## 授权用户类型 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e05abbce6453450fb38747101cb5e228}

**输入(setAssetPermissonsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要处理的文件夹的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 文件夹句柄。 |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | 是 | 权限阵列。 |

**输出(setAssetPermissonsReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-38955bc330bb4909b6b06027ef2b143e}

此代码示例可设置资产的权限。 它包含公司和资产句柄以及权限数组。

**请求**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**响应**

无。
