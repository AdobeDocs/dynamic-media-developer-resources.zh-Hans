---
description: 更新現有資產集的集定義。
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 6%

---

# setAssetSetDefinition{#setassetsetdefinition}

更新現有資產集的集定義。

语法

## 授權的使用者型別 {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**輸入(setAssetDefinitionParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 資產集所在公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 資產集控制代碼 |
| setDefinition | `xsd:string` | 是 | 定義字串。 請參閱下文。 |

**輸出(setAssetSetDefinitionReturn)**

IPS API未傳回此作業的回應。

## setDefinition引數：關於 {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition函式**

指定 `setDefinition` 替代函式內嵌。 這些問題會在目錄查閱期間或發佈時解決。 替代字串的格式為 `${<substitution_func>}`，並包含下列專案：

>[!NOTE]
>
>引數清單中的處理常值必須以方括弧括住 `([])`. 在解析期間，替代字串之外的文字會複製到輸出字串。

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 替代函式 </th> 
   <th colname="col2" class="entry"> 傳回資產的 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 主要檔案路徑。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 目錄ID。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>]，[ <span class="varname"> metadata_field_handle </span>]) </span> </td> 
   <td colname="col2"> 中繼資料值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 目錄ID。 套用至影像型資產（影像、調整後的檢視、圖層檢視）。 <p>若是其他資產，則傳回縮圖資產的目錄ID （若有）。 如果沒有任何縮圖資產與資產相關聯，此函式會傳回空字串。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition範例**

此媒體集定義字串：

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

在查詢或發佈時間解析為下列內容：

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## 示例 {#section-739b42eec3074cafae285ec015a2d088}

**请求**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**响应**

无。
