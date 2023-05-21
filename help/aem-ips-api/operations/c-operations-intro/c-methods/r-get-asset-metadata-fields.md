---
description: 傳回所有中繼資料欄位，依資產型別分組。
solution: Experience Manager
title: getassetmetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 23%

---

# getassetmetadataFields{#getassetmetadatafields}

傳回所有中繼資料欄位，依資產型別分組。

语法

## 授權的使用者型別 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**輸入(getAssetMetadataFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 您要擷取其中繼資料之公司的控制代碼。 |

**輸出(getAssetMetadataFieldsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | 是 | 依資產型別排列的中繼資料欄位陣列。 |

## 示例 {#section-d79ab85f29144635b0b61416e52f4f3f}

**请求**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**响应**

>[!NOTE]
>
>為簡短起見，已截斷。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
