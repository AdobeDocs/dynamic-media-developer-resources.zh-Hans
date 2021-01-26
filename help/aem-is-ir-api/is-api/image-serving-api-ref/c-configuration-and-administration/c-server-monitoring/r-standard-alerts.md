---
description: 标准警报在配置的平均时间间隔结束时与合并的电子邮件一起发送。
seo-description: 标准警报在配置的平均时间间隔结束时与合并的电子邮件一起发送。
seo-title: 标准警报
solution: Experience Manager
title: 标准警报
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d3294434-a44b-4742-9d77-a6945760d33c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---


# 标准警报{#standard-alerts}

标准警报在配置的平均时间间隔结束时与合并的电子邮件一起发送。

下表介绍了每种类型的标准警报。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>警报类型</b> </th> 
   <th class="entry"> <b>标题ID</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>锁定的请求 </p> </td> 
   <td> <p>锁定 </p> </td> 
   <td> <p>当请求无法在指定阈值内向客户端返回响应时发送。 可以表示挂起请求，这可能导致Java线程池耗尽。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高并发性 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 当同时处理的请求数(<i>overlap</i>)超过指定阈值时发出。 可以表示服务器过载情况。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小流量 </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>当总请求速率低于指定阈值时生成。 通常指示服务器通信问题（例如，当服务器脱机时）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>错误率 </p> </td> 
   <td> <p>错误 </p> </td> 
   <td> <p>当采样间隔内HTTP错误响应的平均速率超过指定阈值时发出。 可以指示配置问题、缺少图像、网站编程或数据库错误。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>响应时间 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>当采样间隔期间的平均请求处理时间增长超过指定阈值时发送。 通常指示服务器或后端映像存储系统的临时或持续过载情况。 </p> <p>计算平均响应时间时不考虑错误响应。 </p> </td> 
  </tr> 
 </tbody> 
</table>

