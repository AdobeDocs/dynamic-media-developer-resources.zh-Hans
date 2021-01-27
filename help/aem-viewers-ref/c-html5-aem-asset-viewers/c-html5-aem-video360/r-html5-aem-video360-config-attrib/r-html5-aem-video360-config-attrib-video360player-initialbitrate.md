---
description: Video360查看器的配置属性。
seo-description: Video360查看器的配置属性。
seo-title: Video360Player.initialbitrate
solution: Experience Manager
title: Video360Player.initialbitrate
topic: Dynamic Media
uuid: a23fa941-6dd2-41c0-aca9-06f0cdb027b1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 8%

---


# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360查看器的配置属性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 设置用于在桌面上初始播放视频的视频比特率（以k位／秒或kbps为单位）。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器将开始具有下一个较低比特率的视频。 </p> <p>如果设置为<span class="codeph"> 0</span>，则视频播放器会从最低的可能比特率开始。 </p> <p>仅适用于不支持HTML5 HLS视频（如Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器）的系统，以及当播放模式设置为自动时。 </p> </td> 
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

