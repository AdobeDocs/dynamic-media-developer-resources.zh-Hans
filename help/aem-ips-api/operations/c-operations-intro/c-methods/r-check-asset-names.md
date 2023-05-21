---
description: 比較資產名稱與公司影像伺服/影像轉譯目錄名稱空間的所有名稱，以檢查IPS ID衝突。
solution: Experience Manager
title: checkAssetName
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 12%

---

# checkAssetName{#checkassetnames}

比較資產名稱與公司影像伺服/影像轉譯目錄名稱空間的所有名稱，以檢查IPS ID衝突。

语法

## 授權的使用者型別 {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 引數 {#section-9c75b00f2072453abea0bdefc6ad7c99}

**輸入(checkAssetNamesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 包含使用者的公司的控制代碼。 |
| assetNamesArray | `types:StringArray` | 是 | 要檢查的資產名稱陣列。 |

**輸出(checkAssetNamesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | 是 | 使用中的資產名稱陣列。 |

## 示例 {#section-bc5d120d74614a63a425ca3acc337219}

此範常式式碼會要求指定公司使用的資產名稱。 回應會傳回使用中的資產名稱陣列。

**请求**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**响应**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
