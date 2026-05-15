---
description: 标准警报在配置的平均间隔结束时随整合电子邮件消息一起发送。
solution: Experience Manager
title: 标准警报
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
TQID: 'https://experienceleague.adobe.com/EJzmjshgrIk8hpvZvljpsWTHSI-mG67UNAg2NVjBcZg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 0%

---

# 标准警报{#standard-alerts}

标准警报在配置的平均间隔结束时随整合电子邮件消息一起发送。

下表描述了每种类型的标准警报。

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>警报类型</b> </th> 
   <th class="entry"> <b>标题ID</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>锁定的请求 </p> </td> 
   <td> <p>鎖定 </p> </td> 
   <td> <p>当请求未能在指定的阈值内向客户端返回响应时发送。 可以表示挂起的请求，这可能会导致Java线程池耗尽。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>高并发性 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 当并发处理的请求数（<i>重叠</i>）超过指定的阈值时发出。 可指示服务器过载情况。 </td> 
  </tr> 
  <tr> 
   <td> <p>最小流量 </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>当总体请求率低于指定阈值时生成。 通常表示服务器通信问题（例如，服务器离线时）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>错误率 </p> </td> 
   <td> <p>错误 </p> </td> 
   <td> <p>当采样间隔期间HTTP错误响应的平均速率超过指定的阈值时发出。 可以指示配置问题、缺少图像、网站编程或数据库错误。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>响应时间 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>当取样间隔内的平均请求处理时间超过指定阈值时发送。 通常表示服务器或后端图像存储系统的临时或永久过载情况。 </p> <p>计算平均响应时间时不考虑错误响应。 </p> </td> 
  </tr> 
 </tbody> 
</table>
