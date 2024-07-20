---
title: SmartCropVideoPlayer.singleclick
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

智能裁剪视频查看器的配置属性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`无|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按到切换播放/暂停的映射。 设置为<span class="codeph"> none</span>可禁用通过单击/点按进行播放/暂停的功能。 如果设置为<span class="codeph"> playPause</span>，则单击视频可在播放和暂停视频之间切换。 在某些设备上，您可以使用本机控件。 在这种情况下，<span class="codeph"> singleclick</span>行为已禁用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
