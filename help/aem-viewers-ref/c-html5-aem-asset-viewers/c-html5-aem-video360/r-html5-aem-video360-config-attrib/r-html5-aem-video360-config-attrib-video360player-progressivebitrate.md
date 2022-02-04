---
title: Video360Player.progressivebitrate
description: Video360查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 8%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360查看器的配置属性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 指定在当前系统不支持自适应视频播放的情况下从自适应视频集播放的所需视频比特率（千比特/秒或千比特/秒）。 </p> <p>该组件选取尽可能接近（但不超过）指定值的比特率的视频流。 如果自适应视频集中的所有视频流的质量都高于指定的值，则逻辑会选择质量最低的比特率。 </p> </td> 
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
