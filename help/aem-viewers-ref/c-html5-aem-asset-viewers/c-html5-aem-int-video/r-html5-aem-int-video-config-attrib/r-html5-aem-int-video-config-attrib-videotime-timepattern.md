---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,User
exl-id: de071adf-6c3c-4702-8950-8246b8ee459e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

交互式视频查看器的配置属性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置在控制栏中显示的时间模式，其中<span class="codeph"> h</span>表示小时，<span class="codeph"> m</span>表示分钟，<span class="codeph"> s</span>表示秒。 </p> <p>每个时间单位使用的字母数决定了该单位要显示的位数。 如果数字不能满足给定位数，则以后的单位显示等效值。 </p> <p>例如，如果当前影片时间为67分钟5秒，则<span class="codeph"> m:ss</span>的时间模式显示为67:05。 如果时间模式为<span class="codeph"> h:mm:s</span>，则该时间将显示为1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
