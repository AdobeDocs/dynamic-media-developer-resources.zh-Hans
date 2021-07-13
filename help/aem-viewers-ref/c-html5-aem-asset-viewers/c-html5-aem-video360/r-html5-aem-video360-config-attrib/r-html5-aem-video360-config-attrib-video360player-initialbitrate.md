---
description: Video360查看器的配置属性。
solution: Experience Manager
title: Video360Player.initialbitrate
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360查看器的配置属性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 设置用于在桌面上初始播放视频的视频比特率（以kbits/秒或kbps为单位）。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器将从具有下一个较低比特率的视频开始。 </p> <p>如果设置为<span class="codeph"> 0</span> ，则视频播放器会从最低的比特率开始。 </p> <p>仅适用于不支持HTML5 HLS视频的系统（例如Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器），以及将播放模式设置为自动时。 </p> </td> 
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
