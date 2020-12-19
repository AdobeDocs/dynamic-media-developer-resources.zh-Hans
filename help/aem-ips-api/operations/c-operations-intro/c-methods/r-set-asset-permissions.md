---
description: 使用权限资产设置单个资产的权限。
seo-description: 使用权限资产设置单个资产的权限。
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Scene7 Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 8%

---


# setAssetPermissions{#setassetpermissions}

使用权限资产设置单个资产的权限。

默认情况下，资产会继承父级文件夹的权限。 设置资产权限后，资产将不再继承其父资产的权限，除非您调用`removeAssetPermissions`。

## 授权用户类型{#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e05abbce6453450fb38747101cb5e228}

**输入(setAssetPermissonsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含要处理的文件夹的公司的句柄。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 文件夹句柄。 |
| ` *`permissionArray`*` | `types:PermissionsUpdateArray` | 是 | 权限阵列。 |

**输出(setAssetPermissonsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-38955bc330bb4909b6b06027ef2b143e}

此代码示例设置资产的权限。 它包含公司和资产句柄以及权限数组。

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
