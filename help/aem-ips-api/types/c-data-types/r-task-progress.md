---
description: 任務進度資訊。
solution: Experience Manager
title: 任務進度
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 35e3be1e-ccc2-460c-98c1-bbefab1df699
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 12%

---

# [!DNL TaskProgress]{#taskprogress}

任務進度資訊。

语法

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 任務型別</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 任務型別說明。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 已處理的任務專案數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 目前處理中的任務專案數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 擱置中任務專案（尚未處理）的數量。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 進度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3"> 進度百分比（範圍0.0 - 1.0）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 進度訊息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 上次更新進度資訊的時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：TaskItemProgressArray</span> </td> 
   <td colname="col3"> 工作專案陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 任務狀態</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">值包括： 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> 未知</span>：任務監視器狀態之間轉換時。 </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> 新增</span>：任務監視器已建立，但尚未接受任務。 </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> 處理中</span>：任務監視器正在處理任務。 </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> 正在停止</span>：工作監視器正在停止工作，因為有停止工作要求。 </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> 完成</span>：指派給任務監視器工作的工作已完成。 </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> 已失敗</span>：指出嚴重錯誤。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
