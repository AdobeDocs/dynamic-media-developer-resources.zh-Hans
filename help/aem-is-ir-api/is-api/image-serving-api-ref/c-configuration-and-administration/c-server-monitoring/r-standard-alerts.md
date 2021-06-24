---
description: 在配置的平均时间间隔结束时，标准警报会随合并的电子邮件消息一起发送。
solution: Experience Manager
title: 标准警报
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 标准警报{#standard-alerts}

在配置的平均时间间隔结束时，标准警报会随合并的电子邮件消息一起发送。

下表描述了每种类型的标准警报。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>警报类型</b> </th> 
   <th class="entry"> <b>标题Id</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>锁定的请求 </p> </td> 
   <td> <p>锁定 </p> </td> 
   <td> <p>请求在指定的阈值内无法向客户端返回响应时发送。 可以表示挂起的请求，这可能导致Java线程池耗尽。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高并发性 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 当同时处理的请求数（<i>重叠</i>）超过指定的阈值时发出。 可表示服务器过载情况。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小流量 </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>当总请求率低于指定的阈值时生成。 通常指示服务器通信问题（例如，当服务器脱机时）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>错误率 </p> </td> 
   <td> <p>错误 </p> </td> 
   <td> <p>当采样间隔期间HTTP错误响应的平均速率超过指定的阈值时发出。 可指示配置问题、缺少图像、网站编程或数据库错误。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>响应时间 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>在采样间隔期间的平均请求处理时间增长到超过指定阈值时发送。 通常指示服务器或后端图像存储系统的临时或永久性过载情况。 </p> <p>计算平均响应时间时，不考虑错误响应。 </p> </td> 
  </tr> 
 </tbody> 
</table>
