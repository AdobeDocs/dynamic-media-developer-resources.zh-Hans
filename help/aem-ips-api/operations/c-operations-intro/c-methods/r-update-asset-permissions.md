---
description: 更新资源权限。
solution: Experience Manager
title: updateAssetPermissons
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 20%

---

# updateAssetPermissons{#updateassetpermissons}

更新资源权限。

语法

## 授权用户类型 {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-392cb3076cf84790a32fd913f2b111a3}

**输入(updateAssetPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司句柄。 |
| assetHandle | `xsd:string` | 是 | 资产句柄。 |
| updateArray | `types:PermissionUpdateArray` | 是 | 您希望应用于资源的权限。 |

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
