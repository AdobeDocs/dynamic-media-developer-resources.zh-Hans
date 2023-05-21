---
description: 刪除多個資產。
solution: Experience Manager
title: deleteAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 487f83e6-f713-40e9-a442-e1179b30012c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 16%

---

# deleteAssets{#deleteassets}

刪除多個資產。

语法

## 授權的使用者型別 {#section-a6bc555b8ac840c98835b73fbf838d70}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-4dc888e77d974ac794b553616dd11e86}

**輸入(deleteAssetsParam)**

<table id="table_AAA6845769DB4B129C8A660D0CBA348A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>資產所屬公司的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要刪除的資產陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(deleteAssetsParam)**

<table id="table_0C6D8D51A79248ACA2022DBB754A9B9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> successCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>已成功刪除的資產數目。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningCount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>在作業嘗試刪除資產時產生警告的資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errororcount</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>作業嘗試刪除資產時產生錯誤的資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>與資產關聯的詳細資訊陣列，在作業嘗試刪除資產時產生警告。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>與資產關聯的詳細資訊陣列，在操作嘗試刪除資產時產生錯誤。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-aaad1933bf86479eb6cb476cec7d4587}

此程式碼範例會將控制代碼傳送至公司，並在中設定一系列資產控制代碼 `deleteAssetsParam` 要求網頁服務伺服器。 `deleteAssetsReturn` 傳回2的成功計數，表示兩個資產均已刪除。

**请求**

```java
<deleteAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</deleteAssetsParam>
```

**响应**

```java
<deleteAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</deleteAssetsReturn>
```
