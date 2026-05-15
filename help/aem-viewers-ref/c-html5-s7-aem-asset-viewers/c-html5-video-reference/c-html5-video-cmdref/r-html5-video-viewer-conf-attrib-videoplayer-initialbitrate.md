---
title: VideoPlayer.initialbitrate
description: 视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
TQID: 'https://experienceleague.adobe.com/Z1oVEpUm58QxYopF3XYd66HXHtzLPOrqea2YKzedD0U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">值</span> </p> </td> 
   <td colname="col2"> <p>设置用于在桌面上初始播放视频的视频比特率（以千位/秒或kbps为单位）。 </p> <p>如果此比特率值在自适应视频集中不存在，则视频播放器将启动具有下一个最低比特率的视频。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则视频播放器将从可能的最低比特率开始。 仅适用于对HTML5 HLS视频没有本机支持的系统（Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器），以及播放模式设置为<span class="codeph">自动</span>的情况。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 示例： {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
