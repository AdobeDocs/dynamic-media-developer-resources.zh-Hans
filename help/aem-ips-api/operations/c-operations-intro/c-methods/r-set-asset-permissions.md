---
description: 使用权限资源设置单个资源的权限。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# setAssetPermissions{#setassetpermissions}

使用权限资源设置单个资源的权限。

默认情况下，Assets将继承其父文件夹的权限。 在设置资源的权限后，除非调用`removeAssetPermissions`，否则它不再继承其父级的权限。

## 授权用户类型 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e05abbce6453450fb38747101cb5e228}

**输入(setAssetPermissonsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要处理的文件夹的公司句柄。 |
| assetHandle | `xsd:string` | 是 | 文件夹句柄。 |
| permissionArray | `types:PermissionsUpdateArray` | 是 | 权限数组。 |

**输出(setAssetPermissonsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-38955bc330bb4909b6b06027ef2b143e}

此代码示例设置对资源的权限。 它包含公司和资产句柄以及权限数组。

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
