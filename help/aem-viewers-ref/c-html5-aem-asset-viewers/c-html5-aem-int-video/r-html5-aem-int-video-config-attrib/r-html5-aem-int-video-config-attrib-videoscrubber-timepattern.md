---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
uuid: dc2e7b18-abd7-4b53-a0c4-268ec9cf3cb4
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

交互式视频查看器的配置属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置在时间泡中显示的时间模式，其中<span class="codeph"> h</span>表示小时，<span class="codeph"> m</span>表示分钟，<span class="codeph"> s</span>表示秒。 </p> <p>每个时间单位使用的字母数决定单位要显示的数字数。 如果数字不能容纳给定数字，则在后续单位中显示等效值。 </p> <p>例如，如果当前电影时间为67分5秒，则<span class="codeph"> m:ss</span>的时间模式显示为67:05。 如果时间模式为<span class="codeph"> h:mm:s</span>，则同一时间显示为1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

