---
title: VideoPlayer.playback
description: 視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放型別。 時間 <span class="codeph"> 自動</span> 已設定，在大多數案頭瀏覽器和所有iOS裝置上，檢視器會使用HLS格式的HTML5串流視訊。 它會退回至某些系統(例如舊版Internet Explorer和Android™)上的漸進式HTML5播放。 </p> <p>若 <span class="codeph"> progressive</span> 已指定，則檢視器僅會依瀏覽器原生支援的方式使用HTML5播放，並在所有系統上以漸進方式播放視訊。 </p> <p>如需自動和漸進模式中播放選取的詳細資訊，請參閱Viewer SDK使用手冊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

當檢視器搭配外部視訊使用時忽略。 另請參閱 [外部視訊支援](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
