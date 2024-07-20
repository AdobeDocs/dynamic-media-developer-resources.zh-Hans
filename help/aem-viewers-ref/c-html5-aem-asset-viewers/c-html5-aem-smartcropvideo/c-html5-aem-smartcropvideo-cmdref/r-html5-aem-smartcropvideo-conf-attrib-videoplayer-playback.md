---
title: SmartCropVideoPlayer.playback
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

智能裁剪视频查看器的配置属性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动|渐进式</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 如果设置了<span class="codeph"> auto</span>，则在大多数桌面浏览器和所有iOS设备上，查看器会使用HLS格式的HTML5流视频。 它回退到某些系统(如旧版Internet Explorer和Android™)上的渐进式HTML5播放。 </p> <p>如果指定了<span class="codeph"> progressive</span>，则查看器仅依赖浏览器本机支持的HTML5播放，并在所有系统上逐步播放视频。 </p> <p>有关自动和渐进模式下的播放选择的更多信息，请参阅查看器SDK用户指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

当查看器与外部视频配合使用时忽略。 查看[外部视频支持]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
