---
description: 与特定资产关联的作业日志条目的详细信息。 getAssetJobLogs返回的数据。
solution: Experience Manager
title: AssetJobLog
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: 2c8ebec2-a664-46cd-b843-9893bfa0a9d1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 15%

---

# AssetJobLog{#assetjoblog}

与特定资产关联的作业日志条目的详细信息。 getAssetJobLogs返回的数据。

语法

## 参数 {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作业处理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作业名称. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">作业日志中的消息。 <p><span class="codeph"> </span> logMessageresponse字段根据authHeaderlocale字段进 <span class="codeph"> </span> 行本地化。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 日志条目中的作业类型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 提交了作业的用户的电子邮件。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 工作日期。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：JobLogDetailArray</span> </td> 
   <td colname="col3"> 每个作业日志的辅助作业日志消息数组。 </td> 
  </tr> 
 </tbody> 
</table>
