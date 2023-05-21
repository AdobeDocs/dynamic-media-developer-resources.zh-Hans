---
description: 各自獨立移動多個資產。 它會使用assetMoveArray中包含的AssetMove型別完成此操作。 每個AssetMove欄位都包含一個目標資料夾。
solution: Experience Manager
title: moveAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 12%

---

# moveAssets{#moveassets}

各自獨立移動多個資產。 它會使用assetMoveArray中包含的AssetMove型別完成此操作。 每個AssetMove欄位都包含一個目標資料夾。

语法

## 授權的使用者型別 {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-7d47f663474b41cc83439288ac133cc5}

**輸入(moveAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 擁有要移動資產之公司的控制代碼。 |
| assetMoveArray | `types:AssetMoveArray` | 是 | 資產移動陣列。 它包含資產和資產目的地資料夾。 |

**輸出(moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 已成功移動資產計數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 作業嘗試移動時產生警告的資產計數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errororcount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 作業嘗試移動時發生錯誤的資產計數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>包含： 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">拋出警告的資產。 </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">警告代碼。 </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">警告的原因。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>包含： 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">擲回錯誤的資產。 </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">錯誤代碼。 </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">錯誤原因。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

此程式碼範例將資產移動至指定的特定位置。 `assetMoveArray`. 陣列包含資產控制代碼及其資料夾控制代碼。 回應指出資產已成功移動。

**请求**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**响应**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```
