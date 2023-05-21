---
title: VideoPlayer.preload
description: 指出檢視器是否在播放開始之前開始載入視訊內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# VideoPlayer.preload{#videoplayer-preload}

指出檢視器是否在播放開始之前開始載入視訊內容。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 若設為 <span class="codeph"> 1 </span> 視訊會在設定資產後立即開始下載，否則只有在使用者起始播放或API呼叫後，才會開始預先載入。 </p> <p>若設為 <span class="codeph"> 0 </span> 某些功能可能要在播放開始後才能運作；具體而言，搜尋作業不會更新視訊影格。 如果停用海報影像，檢視器會顯示為空白區域，而非第一個視訊影格。 </p> <p>某些版本的Internet Explorer 11和Edge瀏覽器可能會忽略停用視訊預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
