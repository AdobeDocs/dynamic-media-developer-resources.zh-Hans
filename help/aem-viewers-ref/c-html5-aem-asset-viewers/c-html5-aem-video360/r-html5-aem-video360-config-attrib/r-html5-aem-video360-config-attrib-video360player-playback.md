---
title: Video360Player.playback
description: Video360 Viewer的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 1%

---

# Video360Player.playback{#video-player-playback}

Video360 Viewer的配置属性。

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动|渐进式</span> </p> </td> 
   <td colname="col2"> <p> 设置查看器使用的播放类型。 </p> <p>如果设置了<span class="codeph"> auto</span>，则在大多数桌面浏览器和所有iOS设备中，查看器会使用HLS格式的HTML5流视频。 此外，它回退到某些系统(如旧版Internet Explorer和Android™)上的渐进式HTML5播放。 </p> <p>当设置<span class="codeph"> progressive</span>时，查看器仅依赖浏览器本机支持的HTML5播放，并在所有系统上逐步播放视频。 </p> <p>有关<span class="codeph">自动</span>和<span class="codeph">渐进式</span>本机模式下播放选择的更多信息，请参阅HTML5查看器SDK用户指南。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。 当查看器与外部视频配合使用时忽略。

有关详细信息，请参阅[外部视频支持](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
