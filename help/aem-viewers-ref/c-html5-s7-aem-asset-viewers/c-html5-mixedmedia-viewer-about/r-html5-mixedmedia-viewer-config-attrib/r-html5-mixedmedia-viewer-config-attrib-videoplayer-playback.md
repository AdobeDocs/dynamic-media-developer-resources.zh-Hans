---
description: 混合媒体视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

混合媒体视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 当设置<span class="codeph"> auto</span>时，在大多数桌面浏览器和所有iOS设备上，查看器使用HLS格式的HTML5流视频。 这可归结于在某些系统（如旧版Internet Explorer和Android）上渐进式HTML5播放。 </p> <p>如果指定<span class="codeph">渐进式</span>，则查看器仅依赖浏览器本机支持的HTML5播放，并在所有系统上渐进式播放视频。 </p> <p>有关在自动和渐进式模式下播放选择的详细信息，请参阅《Viewer SDK用户指南》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
