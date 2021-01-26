---
description: 更新资产权限。
seo-description: 更新资产权限。
seo-title: updateAssetPermissons
solution: Experience Manager
title: updateAssetPermissons
topic: Dynamic Media Image Production System API
uuid: feb2faf3-81de-436e-82de-1e41df03508f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 22%

---


# updateAssetPermissons{#updateassetpermissons}

更新资产权限。

语法

## 授权用户类型{#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-392cb3076cf84790a32fd913f2b111a3}

**输入(updateAssetPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`updateArray`*` | `types:PermissionUpdateArray` | 是 | 要应用于资产的权限。 |

**输出(updateAssetPermissionsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**请求**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**响应**

无。
