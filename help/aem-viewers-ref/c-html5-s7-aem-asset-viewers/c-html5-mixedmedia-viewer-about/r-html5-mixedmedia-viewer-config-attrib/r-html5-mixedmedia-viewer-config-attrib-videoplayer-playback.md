---
title: VideoPlayer.playback
description: 混合媒體視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

混合媒體視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放型別。 時間 <span class="codeph"> 自動</span> 已設定，在大多數案頭瀏覽器和所有iOS裝置上，檢視器會使用HLS格式的HTML5串流視訊。 它會退回至某些系統(例如舊版Internet Explorer和Android™)上的漸進式HTML5播放。 </p> <p>若 <span class="codeph"> progressive</span> 已指定，則檢視器僅會依瀏覽器原生支援的方式使用HTML5播放，並在所有系統上以漸進方式播放視訊。 </p> <p>如需自動和漸進模式中播放選取的詳細資訊，請參閱Viewer SDK使用手冊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
