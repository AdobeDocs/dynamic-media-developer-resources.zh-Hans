---
title: SmartCropVideoPlayer.singleclick
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

智慧型裁切視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定按一下/點選以切換播放/暫停的對應。 設定為 <span class="codeph"> 無</span> 停用按一下/點選以播放/暫停。 若設為 <span class="codeph"> playPause</span>，按一下視訊可在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在這種情況下， <span class="codeph"> singleclick</span> 行為已停用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
