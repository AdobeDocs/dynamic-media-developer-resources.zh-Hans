---
title: VideoScrubber.timepattern
description: VideoScrubber.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0536110e-a885-4fd4-baa8-742fcdba5cc9
TQID: 'https://experienceleague.adobe.com/kZiCjbfXz2sgKjTDm5a42v5EmbUI-7T-iVcxJIuJmyY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h：]m|mm：s|ss</span> </p> </td> 
   <td colname="col2"> <p> 为时间泡中显示的时间设置模式，其中<span class="codeph"> h</span>是小时，<span class="codeph"> m</span>是分钟，<span class="codeph"> s</span>是秒。 </p> <p>用于每个时间单位的字母数决定了时间单位显示的位数。 如果数字不符合指定的位数，则会在后续单元中显示对等值。 </p> <p>例如，如果当前的电影时间为67分5秒，则时间模式<span class="codeph"> m：ss</span>显示为67:05。 如果给定的时间模式为<span class="codeph"> h:mm:s</span>，则相同的时间显示为1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
