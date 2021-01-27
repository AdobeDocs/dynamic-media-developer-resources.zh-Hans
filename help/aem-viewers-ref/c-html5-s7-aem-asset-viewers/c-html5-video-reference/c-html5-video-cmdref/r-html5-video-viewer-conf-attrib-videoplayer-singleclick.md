---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic Media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`无|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 无|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 配置单击／点按以切换播放／暂停的映射。 设置为<span class="codeph"> none</span>将禁用单击／点按以播放／暂停。 如果设置为<span class="codeph"> playPause</span>，则单击视频在播放和暂停视频之间切换。 在某些设备上，您可以使用本机控件。 在这种情况下，<span class="codeph"> singlick</span>行为被禁用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```

