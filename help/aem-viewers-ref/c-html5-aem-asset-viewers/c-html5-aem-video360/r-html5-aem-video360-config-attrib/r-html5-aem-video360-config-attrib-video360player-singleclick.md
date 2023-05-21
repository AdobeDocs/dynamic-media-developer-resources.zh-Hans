---
title: Video360Player.singleclick
description: Video360 Viewer的設定屬性。
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

Video360 Viewer的設定屬性。

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 設定按一下/點選以切換播放/暫停的對應。 設定為 <span class="codeph"> 無</span> 停用按一下/點選以播放/暫停。 若設為 <span class="codeph"> playPause</span>，然後選取視訊可在播放和暫停視訊之間切換。 在某些裝置上，您可以使用原生控制項。 在此案例中， <span class="codeph"> singleclick</span> 行為已停用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
