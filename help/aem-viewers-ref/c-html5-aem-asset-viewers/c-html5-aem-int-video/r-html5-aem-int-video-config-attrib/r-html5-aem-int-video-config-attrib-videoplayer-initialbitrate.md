---
title: VideoPlayer.initialbitrate
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 设置用于在桌面上初始播放视频的视频比特率（以千比特/秒或kbps为单位）。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器将从具有下一个较低比特率的视频开始。 </p> <p>如果设置为<span class="codeph"> 0</span>，则视频播放器会从尽可能低的比特率开始。 </p> <p>仅适用于不支持HTML5 HLS视频的系统（例如Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器），以及将播放模式设置为自动时。 </p> </td> 
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
