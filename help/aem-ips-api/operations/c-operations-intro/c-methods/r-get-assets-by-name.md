---
description: 根據資產名稱的陣列傳回資產。
solution: Experience Manager
title: getAssetsByName
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e48574e3-9d16-45fb-b4c8-98b5e092e611
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 15%

---

# getAssetsByName{#getassetsbyname}

根據資產名稱的陣列傳回資產。

语法

## 授權的使用者型別 {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>僅傳回使用者有讀取存取權的資產。

## 参数 {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**輸入(getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 提供存取權給其他使用者。 僅供管理員使用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用於依特定群組篩選。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 要擷取的資產名稱陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 擷取資產允許的資產型別陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 為擷取的資產排除的資產型別陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 擷取資產允許的資產子型別陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>若 <span class="codeph"> true</span> 和 <span class="codeph"> assetSubTypeArray</span> 不是空的，只有子型別位於以下位置的資產： <span class="codeph"> assetSubTypeArray</span> 會傳回。 </p> <p>若 <span class="codeph"> false</span>，則包含未定義子型別的資產。 </p> <p>預設值為 <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含回應中包含的欄位和子欄位清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含從回應中排除的欄位和子欄位清單。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getAssetsByNameReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetArray | `types:AssetArray` | 否 | 符合篩選條件的資產陣列。 |

## 示例 {#section-3b7447398e574c88aeaf8ca159cc78dd}

此程式碼範例會傳回兩個影像型別資產。

**请求**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**响应**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```
