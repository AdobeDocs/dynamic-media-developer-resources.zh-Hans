---
description: 从所选资源中删除权限。
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
TQID: 'https://experienceleague.adobe.com/x8k6HwyFQ-U1VHnFmPAPPPuN9pftPorvmXnIWhXfI3k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 14%

---

# removeAssetPermissions{#removeassetpermissions}

从所选资源中删除权限。

语法

## 授权用户类型 {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**输入(removeAssetPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的把手。 |
| assetHandle | `xsd:string` | 是 | 具有要删除的权限的资源的句柄。 |

**输出(removeAssetPermissionsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-238fa7bb091548f5ba72ced11fc92d4f}

此代码示例从资源中删除权限。

**请求**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**响应**

无。

