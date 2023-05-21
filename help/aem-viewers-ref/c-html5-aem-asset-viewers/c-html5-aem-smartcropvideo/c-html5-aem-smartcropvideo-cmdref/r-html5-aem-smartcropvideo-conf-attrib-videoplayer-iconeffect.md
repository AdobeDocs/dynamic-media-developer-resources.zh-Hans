---
title: SmartCropVideoPlayer.iconeffect
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

智慧型裁切視訊檢視器的設定屬性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`淡化`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 啟用IconEffect，以便在視訊暫停時顯示在視訊上方。 在某些裝置上，會使用原生控制項。 在這種情況下， <span class="codeph"> iconeffect</span> 修飾元會被忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出現和重新出現的最大次數。 值 <span class="codeph"> -1</span> 表示圖示會無限期地重新出現。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡化</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> 設定IconEffect在自動隱藏前保持可見的秒數。 亦即，淡入動畫完成之後和淡出動畫開始之前的時間。 設定 <span class="codeph"> 0</span> 停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
