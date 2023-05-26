---
title: VideoPlayer.singleclick
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

交互式视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

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
