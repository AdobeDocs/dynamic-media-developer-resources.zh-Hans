---
description: 移除所選資產的許可權。
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# removeAssetPermissions{#removeassetpermissions}

移除所選資產的許可權。

语法

## 授權的使用者型別 {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**輸入(removeAssetPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 具有您要移除之許可權的資產的控點。 |

**輸出(removeAssetPermissionsReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-238fa7bb091548f5ba72ced11fc92d4f}

此程式碼範例會從資產中移除許可權。

**请求**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**响应**

无。
