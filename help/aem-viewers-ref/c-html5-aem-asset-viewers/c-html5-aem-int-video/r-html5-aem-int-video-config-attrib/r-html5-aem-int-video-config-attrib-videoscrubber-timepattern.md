---
title: VideoScrubber.timepattern
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
TQID: 'https://experienceleague.adobe.com/ZNw6n5Zokz-s696GvaLkQJY-fAT-JoNafyLzpztZqos'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

交互式视频查看器的配置属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h：]m|mm：s|ss</span> </p> </td> 
   <td colname="col2"> <p> 为时间泡中显示的时间设置模式，其中<span class="codeph"> h</span>表示小时，<span class="codeph"> m</span>表示分钟，<span class="codeph"> s</span>表示秒。 </p> <p>用于每个时间单位的字母数决定了时间单位显示的位数。 如果数字不符合指定的位数，则会在后续单元中显示对等值。 </p> <p>例如，如果当前的电影时间为67分5秒，则时间模式<span class="codeph"> m：ss</span>显示为67:05。 如果时间模式为<span class="codeph"> h:mm:s</span>，则相同的时间显示为1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## 示例： {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
