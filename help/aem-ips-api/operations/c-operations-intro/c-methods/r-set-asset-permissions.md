---
description: 使用許可權資產設定單一資產的許可權。
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 9%

---

# setAssetPermissions{#setassetpermissions}

使用許可權資產設定單一資產的許可權。

資產預設會繼承其父資料夾的許可權。 設定資產的許可權後，除非您呼叫，否則資產不再繼承其父級的許可權 `removeAssetPermissions`.

## 授權的使用者型別 {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e05abbce6453450fb38747101cb5e228}

**輸入(setAssetPermissonsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含您要使用之資料夾的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 資料夾控制代碼。 |
| permissionArray | `types:PermissionsUpdateArray` | 是 | 許可權陣列。 |

**輸出(setAssetPermissonsReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-38955bc330bb4909b6b06027ef2b143e}

此程式碼範例會設定資產的許可權。 它包含公司和資產控點，以及許可權陣列。

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
