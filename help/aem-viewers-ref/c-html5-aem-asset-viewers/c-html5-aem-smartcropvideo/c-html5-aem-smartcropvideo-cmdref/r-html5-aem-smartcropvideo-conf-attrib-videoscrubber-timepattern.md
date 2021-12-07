---
title: VideoScrubber.timepattern
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

智能裁剪视频查看器的配置属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 设置在时间气泡中显示的时间的模式，其中 <span class="codeph"> h</span> 是小时， <span class="codeph"> m</span> 是分钟，并且 <span class="codeph"> s</span> 为秒。 </p> <p>每个时间单位使用的字母数决定了该单位要显示的位数。 如果数字不能满足给定位数，则以后的单位显示等效值。 </p> <p>例如，如果当前影片时间为67分5秒，则时间模式为 <span class="codeph"> m:ss</span> 显示为67:05。 同一时间显示为1:07:5如果给定的时间模式为 <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
