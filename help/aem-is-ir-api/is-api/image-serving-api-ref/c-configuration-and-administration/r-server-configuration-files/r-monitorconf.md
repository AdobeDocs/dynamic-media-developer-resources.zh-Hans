---
description: 包含监控/警报系统的设置。
solution: Experience Manager
title: monitor.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 09c30680-dd9f-4744-b5ec-105721058883
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# monitor.conf{#monitor-conf}

包含监控/警报系统的设置。

此文件是一个JAVA属性文件。 必须注意遵循适当的惯例；否则[!DNL Platform Server]可能无法启动。 请特别注意，在Windows文件路径中，必须使用双反斜杠“\\”或单正斜杠“/”，而不是反斜杠“\”，因为反斜杠在此类型的文件中用作转义字符。

对此文件所做的更改将在保存文件后不久生效。

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>常规 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1 </span> </p> <p> <span class="codeph"> mailSender.port=25 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>警报阈值 </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>
