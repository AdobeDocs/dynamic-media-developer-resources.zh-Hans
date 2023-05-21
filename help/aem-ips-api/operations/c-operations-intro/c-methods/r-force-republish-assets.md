---
description: 重設一或多個資產的發佈狀態，以強制在下個發佈工作中重新發佈資產。
solution: Experience Manager
title: Forcerepublishassets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4c75af38-4791-4f21-8d1b-4855fcdfd4b1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 12%

---

# Forcerepublishassets{#forcerepublishassets}

重設一或多個資產的發佈狀態，以強制在下個發佈工作中重新發佈資產。

语法

## 授權的使用者型別 {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**輸入(forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>包含要重設之資產的公司的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> 重新發佈檔案</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定將資產的檔案重新發佈至傳送伺服器。 預設為 <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定用於提供資產的目錄中繼資料已同步，以確保其為最新狀態。 此引數用於解決同一記錄的幾乎同時更新時可能發生的競爭條件。 預設為 <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：HandleArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>發佈狀態要重設的資產控制代碼陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>發佈狀態更新的陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>
