---
description: Video360查看器的配置属性。
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 6%

---

# Video360Player.playback{#video-player-playback}

Video360查看器的配置属性。

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动/渐进</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 </p> <p>设置<span class="codeph"> auto</span>后，在大多数桌面浏览器和所有iOS设备中，查看器会以HLS格式使用HTML5流视频，并在某些系统（如旧版Internet Explorer和Android）上回退到渐进式HTML5播放。 </p> <p>设置<span class="codeph">渐进式</span>后，查看器仅依赖浏览器本地支持的HTML5播放，并在所有系统上逐步播放视频。 </p> <p>有关<span class="codeph"> auto</span>和<span class="codeph"> progressive</span>本机模式中的播放选择的更多信息，请参阅《HTML5查看器SDK用户指南》。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。查看器处理外部视频时忽略。

有关详细信息，请参阅[外部视频支持](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
