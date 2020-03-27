---
description: 混合媒体视频查看器的配置属性。
seo-description: 混合媒体视频查看器的配置属性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.playback{#videoplayer-playback}

混合媒体视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动——渐进</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 设置 <span class="codeph"> 自动</span> 后，在大多数桌面浏览器和所有iOS设备上，查看器使用HLS格式的HTML5流视频。 它回归到某些系统（如旧版Internet Explorer和Android）上渐进式HTML5播放。 </p> <p>如果指 <span class="codeph"> 定渐进式</span> ，则查看器仅依赖HTML5播放（浏览器本身支持），并在所有系统上渐进式播放视频。 </p> <p>有关在自动和渐进模式中选择回放的详细信息，请参阅《Viewer SDK用户指南》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
