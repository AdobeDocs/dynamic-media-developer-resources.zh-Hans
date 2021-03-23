---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
uuid: 2e911d35-155e-4afa-aede-52e9d00ae211
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 指定在当前系统不支持自适应视频播放时从自适应视频集播放的所需视频比特率（以千位/秒或千位/秒）。 </p> <p>该组件选取最接近（但不超过）指定值的比特率的视频流。 如果自适应视频集中的所有视频流的质量都高于指定值，则逻辑将选择质量最低的比特率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```

