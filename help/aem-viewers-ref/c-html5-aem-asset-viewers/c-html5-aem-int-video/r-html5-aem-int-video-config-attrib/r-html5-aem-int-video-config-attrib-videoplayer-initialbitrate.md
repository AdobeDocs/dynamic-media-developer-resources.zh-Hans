---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 设置用于在桌面上初始播放视频的视频的视频比特率（以千位/秒或kbps为单位）。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器将开始具有下一个比特率较低的视频。 </p> <p>如果设置为<span class="codeph"> 0</span>，则视频播放器会从最低比特率开始。 </p> <p>仅适用于不具有对HTML5 HLS视频（如Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器）本机支持的系统，以及当播放模式设置为“自动”时。 </p> </td> 
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

