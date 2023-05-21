---
title: VideoPlayer.progressivebitrate
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

互動式視訊檢視器的設定屬性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 指定萬一目前系統不支援自我調整視訊播放時，要從「自我調整視訊集」播放的所需視訊位元速率(以千位元/秒(kbps)為單位)。 </p> <p>元件會挑選位元速率最接近（但不超過）指定值的視訊資料流。 如果「自我調整視訊集」中的所有視訊串流都具有高於指定值的品質，則邏輯會選擇品質最低的位元速率。 </p> </td> 
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
