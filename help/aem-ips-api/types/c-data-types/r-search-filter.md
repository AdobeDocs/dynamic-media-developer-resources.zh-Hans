---
description: 可協助您定義搜尋條件以提高搜尋效率的篩選器。
solution: Experience Manager
title: SearchFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b3a26966-33c9-48ca-b0ed-d05fc0e2050f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# [!DNL SearchFilter]{#searchfilter}

可協助您定義搜尋條件以提高搜尋效率的篩選器。

语法

## 参数 {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 資料夾</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 指定您要搜尋的資料夾。 留空可在整個公司中搜尋。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">設定為： 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>：搜尋已命名的資料夾和所有子資料夾。 </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>：僅搜尋已命名的資料夾。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type：StringArray</span> </td> 
   <td colname="col3">要在搜尋中傳回的資產型別清單。 例如， <span class="codeph"> 影像</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type：StringArray</span> </td> 
   <td colname="col3"> 指定要從搜尋中排除的資產型別。 例如，影像。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type：StringArray</span> </td> 
   <td colname="col3">搜尋時想要傳回的資產子型別清單。 例如，對於 <span class="codeph"> 資產集</span>，您可以搜尋 <span class="codeph"> MediaType</span> 子型別。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>選用的布林值標幟，可指定是否在 <span class="codeph"> assetSubTypeArray</span> 已通過。 </p> <p>如果為true，則只會傳回具有其中一個指定子型別的資產。 </p> <p>如果為false，則也會傳回沒有子型別的資產。 </p> <p>預設值為false。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">設定為： 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>：僅傳回原始資產。 </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>：傳回產生的內容。 例如，來自已上傳PDF的影像。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 處理您要搜尋的專案。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> 已標籤為發佈</span> 以僅傳回已發佈的資產。 </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> 僅傳回未發佈的資產。 </li> 
    </ul> <p>注意：留空可搜尋 <i>全部</i> 已發佈狀態型別。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">指定: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> 任何</span> 以傳回資產，無論其垃圾桶狀態為何。 </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span> 以傳回「一般」資產。 </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InTrash</span> 以從垃圾桶傳回資產。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
