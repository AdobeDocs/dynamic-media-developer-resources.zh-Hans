---
description: 视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按的映射以切换播放/暂停。 将设置为<span class="codeph"> none</span>会禁用单击/点按播放/暂停。 如果设置为<span class="codeph"> playPause</span>，则单击视频可在播放和暂停视频之间切换。 在某些设备上，您可以使用本机控件。 在这种情况下，<span class="codeph"> singleclick</span>行为被禁用。 </p> </td> 
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
