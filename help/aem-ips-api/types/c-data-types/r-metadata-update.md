---
description: 設定搭配setAssetMetadata使用的特定資產的中繼資料值。 說明您想對中繼資料進行的變更。
solution: Experience Manager
title: 中繼資料更新
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 99dc1f0c-c4c4-433e-9b91-fa39ef6f84d7
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 4%

---

# [!DNL MetadataUpdate]{#metadataupdate}

設定搭配setAssetMetadata使用的特定資產的中繼資料值。 說明您想對中繼資料進行的變更。

>[!NOTE]
>
>如果傳遞了單一值欄位，資產的標籤值會重設為指定的標籤值。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 中繼資料更新值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 布林值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 布林值中繼資料值（僅適用於布林型別欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：long</span> </td> 
   <td colname="col3"> 長中繼資料值（僅適用於int型別的欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleval</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3"> 雙倍中繼資料值（僅適用於浮點型欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 日期值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 日期中繼資料值（僅適用於日期型別欄位）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> <p>新增至資產的現有標籤值清單。 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">單值標籤欄位僅儲存最後一個值。 </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">如果值不在字典中，固定字典標籤欄位會傳回錯誤。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3">取代資產的現有標籤值清單。 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">單值標籤欄位僅儲存最後一個值。 </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">如果值不在字典中，固定字典標籤欄位會傳回錯誤。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：StringArray</span> </td> 
   <td colname="col3"> 從資產的標籤值清單中刪除指定的值（如果存在）。 </td> 
  </tr> 
 </tbody> 
</table>
