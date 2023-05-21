---
title: VideoPlayer.initialbitrate
description: 視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值 </span> </p> </td> 
   <td colname="col2"> <p>設定在桌上型電腦上初始播放視訊所使用的視訊位元速率（以千位元/秒或kbps為單位）。 </p> <p>如果此位元速率值不存在最適化視訊集中，則視訊播放器會啟動具有下一個最低位元速率的視訊。 </p> <p>若設為 <span class="codeph"> 0 </span>，視訊播放器會從最低的位元速率開始。 僅適用於對HTML5 HLS視訊沒有原生支援的系統（Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），且播放模式設定為時 <span class="codeph"> 自動 </span>. </p> </td> 
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
