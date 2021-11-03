---
title: SmartCropVideoPlayer.playback
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

智能裁剪视频查看器的配置属性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动/渐进</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 When <span class="codeph"> 自动</span> 在大多数桌面浏览器和所有iOS设备上设置时，查看器使用HLS格式的HTML5流视频。 它返回到某些系统(如旧版Internet Explorer和Android™)上的渐进式HTML5播放。 </p> <p>如果 <span class="codeph"> 渐进</span> 已指定，则查看器仅依赖浏览器本地支持的HTML5播放，并在所有系统上逐步播放视频。 </p> <p>有关在自动和渐进模式下选择播放的更多信息，请参阅查看器SDK用户指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

查看器处理外部视频时忽略。 请参阅 [外部视频支持]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
