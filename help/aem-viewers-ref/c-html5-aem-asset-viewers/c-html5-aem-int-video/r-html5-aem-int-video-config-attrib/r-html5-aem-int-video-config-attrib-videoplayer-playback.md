---
title: VideoPlayer.playback
description: 互動式視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

互動式視訊檢視器的設定屬性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> 設定檢視器使用的播放型別。 </p> <p>時間 <span class="codeph"> 自動</span> 已設定，在大多數案頭瀏覽器和所有iOS裝置中，檢視器會使用HLS格式的HTML5串流視訊。 此外，它也會退回某些系統(例如舊版Internet Explorer和Android™)上的漸進式HTML5播放。 </p> <p>時間 <span class="codeph"> progressive</span> 設定，則檢視器僅會依瀏覽器原生支援的方式播放HTML5，並在所有系統上以漸進方式播放視訊。 </p> <p>有關中播放選取範圍的詳細資訊 <span class="codeph"> 自動</span> 和 <span class="codeph"> progressive</span> 原生模式，請參閱HTML5 Viewers SDK使用手冊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
