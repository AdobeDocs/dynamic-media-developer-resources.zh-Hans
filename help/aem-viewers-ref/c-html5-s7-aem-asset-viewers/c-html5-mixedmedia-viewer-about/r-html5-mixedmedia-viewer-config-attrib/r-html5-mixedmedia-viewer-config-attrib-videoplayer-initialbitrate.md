---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
   <td colname="col2"> <p>设置用于在桌面上初始播放视频的视频的视频比特率，以千位/秒或kbps为单位。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器会开始具有下一最低比特率的视频。 </p> <p>如果设置为<span class="codeph"> 0 </span> ，则视频播放器会从最低比特率开始。 仅适用于不具有对HTML5 HLS视频（Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器）本机支持的系统，以及当播放模式设置为<span class="codeph">自动</span>时。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
