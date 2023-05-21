---
title: Video360Player.initialbitrate
description: Video360 Viewer的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 6%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360 Viewer的設定屬性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 設定在案頭上初始播放視訊時使用的視訊位元速率（以千位元/秒或kbps為單位）。 </p> <p>如果「自我調整視訊集」中不存在此位元速率值，則視訊播放器會從擁有次低位元速率的視訊開始。 </p> <p>若設為 <span class="codeph"> 0</span>，視訊播放器會從最低的位元速率開始。 </p> <p>僅適用於對HTML5 HLS視訊沒有原生支援的系統（例如Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），以及播放模式設定為auto時。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
