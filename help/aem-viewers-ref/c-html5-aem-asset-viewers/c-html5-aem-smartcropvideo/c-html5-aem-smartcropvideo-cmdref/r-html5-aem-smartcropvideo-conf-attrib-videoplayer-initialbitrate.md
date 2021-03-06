---
title: SmartCropVideoPlayer.initialbitrate
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4fc4fefa-b094-4e2e-b8ec-a439f8a1a56c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

视频查看器的配置属性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值 </span> </p> </td> 
   <td colname="col2"> <p>设置用于在桌面上初始播放视频的视频比特率（以千比特/秒或kbps为单位）。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器会启动比特率最低的视频。 </p> <p>如果设置为 <span class="codeph"> 0 </span>，则视频播放器将从尽可能低的比特率开始。 仅适用于不支持HTML5 HLS视频（在Windows 10上为Firefox、Chrome和Internet Explorer 11浏览器）的本机系统，以及将播放模式设置为 <span class="codeph"> 自动 </span>. </p> </td> 
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
