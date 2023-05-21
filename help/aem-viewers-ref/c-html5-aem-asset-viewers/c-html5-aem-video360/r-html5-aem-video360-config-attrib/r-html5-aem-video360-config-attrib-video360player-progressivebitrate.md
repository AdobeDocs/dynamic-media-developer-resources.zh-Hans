---
title: Video360Player.progressivebitrate
description: Video360 Viewer的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360 Viewer的設定屬性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 指定目前系統不支援自我調整視訊播放時，要從「自我調整視訊集」播放的所需視訊位元速率（以千位元/秒或kbps為單位）。 </p> <p>元件會挑選位元速率最接近（但不超過）指定值的視訊資料流。 如果「自我調整視訊集」中的所有視訊串流都具有高於指定值的品質，則邏輯會選擇品質最低的位元速率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
