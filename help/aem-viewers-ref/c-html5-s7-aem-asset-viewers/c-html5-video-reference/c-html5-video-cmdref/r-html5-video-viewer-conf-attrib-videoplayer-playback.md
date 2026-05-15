---
title: VideoPlayer.playback
description: 视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
TQID: 'https://experienceleague.adobe.com/kWCkzBjr6vJAyCk6PareJcg8AfwNvm2gNcEC5BpZXxE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动|渐进式</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 如果设置了<span class="codeph"> auto</span>，则在大多数桌面浏览器和所有iOS设备上，查看器将使用HLS格式的HTML5流视频。 它回退到某些系统（如旧版Internet Explorer和™）上的渐进式HTML5播放。 </p> <p>如果指定了<span class="codeph"> progressive</span>，则查看器仅依赖浏览器本机支持的HTML5播放，并在所有系统上逐步播放视频。 </p> <p>有关自动和渐进模式下的播放选择的更多信息，请参阅查看器SDK用户指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

当查看器与外部视频配合使用时忽略。 请参阅[外部视频支持](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例： {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
