---
description: 使用者定義的特定資產欄位定義。
solution: Experience Manager
title: MetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 97175076-9078-4bc4-b3ea-73c3ea772f6a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 15%

---

# [!DNL MetadataField]{#metadatafield}

使用者定義的特定資產欄位定義。

使用擷取標籤欄位定義 `getMetadataFields` 或 `getAssetMetadataField` 作業。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 中繼資料欄位控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 中繼資料欄位名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 中繼資料欄位型別。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 預設值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 中繼資料欄位的預設值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 必填</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 設定必要的狀態。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isUserDefined</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 判斷中繼資料欄位是否由使用者定義。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> ishidden</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">隱藏或公開IPS系統特定的中繼資料。 傳回自 <a href="../../operations/c-operations-intro/c-methods/r-get-metadata-fields.md#reference-170337127801401d9ea54bd4ccf28efe" format="dita" scope="local"> getMetadataFields</a> 和 <a href="../../operations/c-operations-intro/c-methods/r-get-asset-metadata-fields.md#reference-ea57f8e98d3e443da66114550b0d0a28" format="dita" scope="local"> getassetmetadataFields</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>布林值標幟，指出在設定值時，是否強制執行（驗證）中繼資料欄位型別。 </p> <p>若設為true，則若在中設定了不合法的值，則會擲回錯誤 <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTag值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 可讓您建立一組所選標籤可指向的共用列舉值。 </td> 
  </tr> 
 </tbody> 
</table>
