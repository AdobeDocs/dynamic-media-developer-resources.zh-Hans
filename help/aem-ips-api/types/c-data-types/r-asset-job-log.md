---
description: 与特定资产关联的作业日志条目的详细信息。 getAssetJobLogs返回的数据。
seo-description: 与特定资产关联的作业日志条目的详细信息。 getAssetJobLogs返回的数据。
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Scene7 Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> 作 <span class="varname"> 业处理</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 工作负责人。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作业名称. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">作业日志中的消息。 <p><span class="codeph"> logMessage响应字段</span> ，根据authHeader区域设置字 <span class="codeph"> 段进行本地化</span> 。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 日志条目中的作业类型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> submitUserEmail <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 提交作业的用户的电子邮件。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 工作日期。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:JobLogDetailArray</span> </td> 
   <td colname="col3"> 每个作业日志的辅助作业日志消息数组。 </td> 
  </tr> 
 </tbody> 
</table>

