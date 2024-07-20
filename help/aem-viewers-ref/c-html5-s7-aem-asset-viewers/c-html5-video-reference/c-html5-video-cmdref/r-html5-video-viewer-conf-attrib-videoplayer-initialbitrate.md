---
title: VideoPlayer.initialbitrate
description: 视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">值</span> </p> </td> 
   <td colname="col2"> <p>设置用于在桌面上初始播放视频的视频比特率（以千位/秒或kbps为单位）。 </p> <p>如果此比特率值在自适应视频集中不存在，则视频播放器将启动具有下一个最低比特率的视频。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则视频播放器将从可能的最低比特率开始。 仅适用于对HTML5 HLS视频没有本机支持的系统(Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器)，以及播放模式设置为<span class="codeph">自动</span>的情况。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
