---
title: Video360Player.singleclick
description: Video360 Viewer的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 10%

---

# Video360Player.singleclick{#video-player-singleclick}

Video360 Viewer的配置属性。

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按到切换播放/暂停的映射。 将设置为 <span class="codeph"> 无</span> 禁用单击/点按以播放/暂停。 如果设置为 <span class="codeph"> playPause</span>，然后选择视频可在播放和暂停视频之间切换。 在某些设备上，您可以使用本机控件。 在本例中， <span class="codeph"> singleclick</span> 行为已禁用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
