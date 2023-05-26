---
title: VideoPlayer.playback
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

交互式视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|渐进式</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 </p> <p>时间 <span class="codeph"> 自动</span> 已设置，在大多数桌面浏览器和所有iOS设备中，查看器使用HLS格式的HTML5流视频。 此外，它还可以退回到某些系统(如旧版Internet Explorer和Android™)上的渐进式HTML5播放。 </p> <p>时间 <span class="codeph"> 渐进式</span> ，则查看器仅依赖浏览器本机支持的HTML5播放，并在所有系统上逐步播放视频。 </p> <p>有关中播放选择的更多信息 <span class="codeph"> 自动</span> 和 <span class="codeph"> 渐进式</span> 本机模式，请参阅HTML5 Viewers SDK用户指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
