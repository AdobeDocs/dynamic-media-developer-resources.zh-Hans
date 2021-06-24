---
description: 视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: Developer,Business Practitioner
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值  </span> </p> </td> 
   <td colname="col2"> <p>设置用于在桌面上初始播放视频的视频的视频比特率（以千位/秒为单位）或kbps。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器会启动比特率最低的视频。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则视频播放器会从尽可能低的比特率开始。 仅适用于不支持HTML5 HLS视频（Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器）的系统，以及将播放模式设置为<span class="codeph">自动</span>时。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
