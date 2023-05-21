---
title: Video360Player.preload
description: 指出檢視器是否在播放開始之前開始載入視訊內容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# Video360Player.preload{#video-player-preload}

指出檢視器是否在播放開始之前開始載入視訊內容。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 若設為 <span class="codeph"> 1 </span>，視訊會在設定資產後立即開始下載。 否則，預先載入只有在一般使用者起始播放或API呼叫後才會開始。 </p> <p>若設為 <span class="codeph"> 0 </span>，某些功能可能要在播放開始後才能運作。 具體而言，搜尋作業不會更新視訊影格。 如果停用海報影像，檢視器會顯示為空白區域，而非第一個視訊影格。 </p> <p>某些版本的Internet Explorer 11和Edge瀏覽器可能會忽略停用視訊預先載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
