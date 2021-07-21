---
description: 删除选定资产的权限。
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

---

# removeAssetPermissions{#removeassetpermissions}

删除选定资产的权限。

语法

## 授权用户类型 {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**输入(removeAssetPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 具有您要删除的权限的资产的句柄。 |

**Output(removeAssetPermissionsReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-238fa7bb091548f5ba72ced11fc92d4f}

此代码示例可从资产中删除权限。

**请求**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**响应**

无。
