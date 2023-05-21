---
description: 傳回Zip檔案資料。
solution: Experience Manager
title: getZipEntries
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: eb052685-b750-4a12-b00e-28e676340e98
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 22%

---

# getZipEntries{#getzipentries}

傳回Zip檔案資料。

语法

## 授權的使用者型別 {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-aa3f498fe76d4a5f99c42d64520fadce}

**輸入(getZipEntriesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含Zip檔案之公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | Zip檔案的處理常式。 |

**輸出(getZipEntriesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| zipArray | `types:ZipEntryArray` | 是 | Zip檔案中的專案陣列。 |

## 示例 {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

此程式碼範例會傳回Zip檔案資訊，包括壓縮和未壓縮大小。

**请求**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**响应**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```
