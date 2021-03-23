---
description: 任务进度信息。
seo-description: 任务进度信息。
seo-title: 任务进度
solution: Experience Manager
title: 任务进度
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 11%

---


# TaskProgress{#taskprogress}

任务进度信息。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 任务类型描述。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 已处理的任务项目数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 当前正在处理的任务项数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 待处理任务项（尚未处理）的数量。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 进展</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:多次</span> </td> 
   <td colname="col3"> %进度（范围0.0 - 1.0）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 进度消息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次更新进度信息的时间。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskItemProgressArray</span> </td> 
   <td colname="col3"> 任务项的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">值包括： 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> 未知</span>:当任务监视状态之间过渡时。 </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> 新</span>:任务监视器已创建，但尚未接受任务。 </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> 处理</span>:任务监视器正在主动处理任务。 </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> 正在停止</span>:任务监视器正在停止作业，因为有停止作业请求。 </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> 完成</span>:已完成分配给任务监视器作业的作业。 </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> 失败</span>:表示错误。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

