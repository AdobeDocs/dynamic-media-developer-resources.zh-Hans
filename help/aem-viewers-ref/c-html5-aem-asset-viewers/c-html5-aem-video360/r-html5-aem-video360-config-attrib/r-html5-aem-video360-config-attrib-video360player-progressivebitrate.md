---
description: Video360查看器的配置属性。
seo-description: Video360查看器的配置属性。
seo-title: Video360Player.progressivebitrate
solution: Experience Manager
title: Video360Player.progressivebitrate
topic: Dynamic Media
uuid: 438c18d7-e7ac-4834-8445-def590264448
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 9%

---


# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360查看器的配置属性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 值</span> </p> </td> 
   <td colname="col2"> <p> 指定在当前系统不支持自适应视频播放时从自适应视频集播放的所需视频比特率(以千位／秒（或kbps）为单位)。 </p> <p>该组件以最接近（但不超过）指定值的比特率拾取视频流。 如果自适应视频集中的所有视频流的质量都高于指定值，则逻辑将选择质量最低的比特率。 </p> </td> 
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

