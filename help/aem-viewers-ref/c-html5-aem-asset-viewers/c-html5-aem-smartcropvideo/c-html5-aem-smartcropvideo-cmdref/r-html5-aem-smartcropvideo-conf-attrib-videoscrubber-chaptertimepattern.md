---
title: VideoScrubber.chaptertimepattern
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5552ed9e-d8fe-4723-a360-405b91e27f8e
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

智能裁剪视频查看器的配置属性。

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h：]m|mm：s|ss</span> </p> </td> 
   <td colname="col2"> <p> 为视频章节标签的标题栏中显示的时间设置模式。 此 <span class="codeph"> h</span> 是小时， <span class="codeph"> m</span> 为分钟，并且 <span class="codeph"> s</span> 为秒。 </p> <p>用于每个时间单位的字母数决定了时间单位要显示的位数。 如果数字不符合指定的位数，则会在后续单位中显示对等值。 </p> <p>例如，如果当前的电影时间是67分5秒，则时间模式 <span class="codeph"> m：ss</span> 显示为67:05。 相同时间显示为1:07:5，如果给定的时间模式为 <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
