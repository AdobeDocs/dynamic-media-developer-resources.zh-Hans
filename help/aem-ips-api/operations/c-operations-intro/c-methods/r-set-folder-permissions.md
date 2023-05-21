---
description: 設定檔案夾許可權。
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 15%

---

# setFolderPermissions{#setfolderpermissions}

設定檔案夾許可權。

语法

## 授權的使用者型別 {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-2a41135054954396b40f1228f2e63b42}

**輸入(setFolderPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控點。 |
| folderHandle | `xsd:string` | 是 | 資料夾控制代碼。 |
| setchildren | `xsd:boolean` | 是 | 設定屬於資料夾之子項的許可權。 |
| permissionArray | `types:PermissionUpdateArray` | 是 | 許可權陣列。 |

**輸出(setFolderPermissionsReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-01730da4be874553ab44e3241cdf6357}

此程式碼範例指定公司控制代碼、資料夾控制代碼和許可權陣列，其中包含有關資料夾的詳細資訊。 它會套用父資料夾子項的相同許可權。

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
