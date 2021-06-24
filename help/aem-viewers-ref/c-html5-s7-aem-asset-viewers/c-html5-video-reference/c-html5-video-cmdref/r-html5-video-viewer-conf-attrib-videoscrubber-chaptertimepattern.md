---
description: 视频查看器的配置属性。
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: Developer,Business Practitioner
exl-id: a159153a-c082-4415-9515-7b480282a31f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

视频查看器的配置属性。

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置视频章节标签标题栏中显示的时间模式，其中<span class="codeph"> h</span>为小时，<span class="codeph"> m</span>为分钟，<span class="codeph"> s</span>为秒。 </p> <p>每个时间单位使用的字母数决定了该单位要显示的位数。 如果数字不能满足给定位数，则以后的单位显示等效值。 </p> <p>例如，如果当前影片时间为67分钟5秒，则时间模式<span class="codeph"> m:ss</span>显示为67:05。 如果给定的时间模式为<span class="codeph"> h:mm:s</span>，则该时间将显示为1:07:5。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
