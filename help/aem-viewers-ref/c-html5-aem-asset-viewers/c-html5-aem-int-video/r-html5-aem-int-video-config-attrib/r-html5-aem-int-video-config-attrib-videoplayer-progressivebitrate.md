---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 以kbits/秒（或kbps）为单位，指定在当前系统不支持自适应视频播放时从自适应视频集播放的所需视频比特率。 </p> <p>该组件选取尽可能接近（但不超过）指定值的比特率的视频流。 如果自适应视频集中的所有视频流的质量都高于指定的值，则逻辑会选择质量最低的比特率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
