---
title: VideoScrubber.timepattern
description: VideoScrubber.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0536110e-a885-4fd4-baa8-742fcdba5cc9
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置在时间气泡中显示的时间的模式，其中 <span class="codeph"> h</span> 是小时， <span class="codeph"> m</span> 是分钟，并且 <span class="codeph"> s</span> 为秒。 </p> <p>每个时间单位使用的字母数决定了该单位要显示的位数。 如果数字不能满足给定位数，则以后的单位显示等效值。 </p> <p>例如，如果当前影片时间为67分5秒，则时间模式为 <span class="codeph"> m:ss</span> 显示为67:05。 同一时间显示为1:07:5如果给定的时间模式为 <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
