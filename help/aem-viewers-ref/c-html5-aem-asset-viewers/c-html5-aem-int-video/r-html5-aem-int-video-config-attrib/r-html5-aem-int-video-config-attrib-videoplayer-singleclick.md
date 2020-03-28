---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: VideoPlayer.singlick
solution: Experience Manager
title: VideoPlayer.singlick
topic: Dynamic media
uuid: 5b387eb6-1e09-4506-beea-3f1cf337cb9d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.singlick{#videoplayer-singleclick}

交互式视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 配置单击／点按的映射以切换播放／暂停。 设置为 <span class="codeph"> 无</span> ，将禁用单击／点按播放／暂停。 如果设置为 <span class="codeph"> playPause</span> ，则单击视频可在播放和暂停视频之间切换。 在某些设备上，您可以使用本机控件。 在这种情况下，将禁 <span class="codeph"> 用单击</span> 行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

