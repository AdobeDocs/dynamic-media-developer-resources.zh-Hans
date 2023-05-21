---
title: SmartCropVideoPlayer.playback
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

智慧型裁切視訊檢視器的設定屬性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

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

當檢視器搭配外部視訊使用時忽略。 另請參閱 [外部視訊支援]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
