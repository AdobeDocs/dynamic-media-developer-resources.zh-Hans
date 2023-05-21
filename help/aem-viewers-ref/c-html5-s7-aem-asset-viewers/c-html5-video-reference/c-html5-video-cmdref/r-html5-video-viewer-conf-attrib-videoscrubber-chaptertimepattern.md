---
title: VideoScrubber.chaptertimepattern
description: 視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a159153a-c082-4415-9515-7b480282a31f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

視訊檢視器的設定屬性。

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h：]m|mm：s|ss</span> </p> </td> 
   <td colname="col2"> <p> 設定視訊章節標籤的標題列中顯示的時間模式，其中 <span class="codeph"> h</span> 是小時， <span class="codeph"> m</span> 為分鐘，且 <span class="codeph"> s</span> 是秒。 </p> <p>用於每個時間單位的字母數目決定該單位要顯示的位數。 如果數字不符合指定的位數，則會在後續單位中顯示對等值。 </p> <p>例如，如果目前的影片時間為67分5秒，則時間模式 <span class="codeph"> m：ss</span> 顯示為67:05。 相同時間顯示為1:07:5如果給定的時間模式為 <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
