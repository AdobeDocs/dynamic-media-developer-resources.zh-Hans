---
description: 混合媒体视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

混合媒体视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动/渐进</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 设置<span class="codeph"> auto</span>后，在大多数桌面浏览器和所有iOS设备上，查看器会使用HLS格式的HTML5流视频。 它返回到某些系统（如旧版Internet Explorer和Android）上的渐进式HTML5播放。 </p> <p>如果指定了<span class="codeph">渐进式</span>，则查看器仅依赖浏览器本地支持的HTML5播放，并在所有系统上逐步播放视频。 </p> <p>有关在自动和渐进模式下选择播放的更多信息，请参阅查看器SDK用户指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
