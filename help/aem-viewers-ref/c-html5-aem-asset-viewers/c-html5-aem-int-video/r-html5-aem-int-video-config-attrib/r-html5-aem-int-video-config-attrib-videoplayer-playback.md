---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 2576f433-b9c2-4da1-9a51-f66b71d5df99
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.playback{#videoplayer-playback}

交互式视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动——渐进</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 </p> <p>设置 <span class="codeph"> 自动</span> 后，在大多数桌面浏览器和所有iOS设备中，查看器使用HLS格式的HTML5流视频，并回到某些系统（如旧版Internet Explorer和Android）上渐进式HTML5回放。 </p> <p>设置 <span class="codeph"> 渐进式</span> 时，查看器仅依赖HTML5播放（浏览器本机支持），并在所有系统上渐进式播放视频。 </p> <p>有关在自动和渐进式本机模式中 <span class="codeph"> 选择播放</span><span class="codeph"> 的更多信息</span> ，请参阅《HTML5查看器SDK用户指南》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
