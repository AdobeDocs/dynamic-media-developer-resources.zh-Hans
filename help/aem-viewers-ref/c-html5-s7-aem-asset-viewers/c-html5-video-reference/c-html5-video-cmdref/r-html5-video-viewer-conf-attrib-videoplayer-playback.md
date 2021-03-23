---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 当设置<span class="codeph"> auto</span>时，在大多数桌面浏览器和所有iOS设备上，查看器使用HLS格式的HTML5流视频。 这可归结于在某些系统（如旧版Internet Explorer和Android）上渐进式HTML5播放。 </p> <p>如果指定<span class="codeph">渐进式</span>，则查看器仅依赖浏览器本机支持的HTML5播放，并在所有系统上渐进式播放视频。 </p> <p>有关在自动和渐进式模式下播放选择的详细信息，请参阅《Viewer SDK用户指南》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

查看器处理外部视频时忽略。 请参阅[外部视频支持](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

