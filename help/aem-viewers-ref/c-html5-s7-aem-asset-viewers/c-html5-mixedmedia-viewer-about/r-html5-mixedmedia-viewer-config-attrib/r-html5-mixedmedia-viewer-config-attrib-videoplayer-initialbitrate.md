---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 4%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
   <td colname="col2"> <p>设置用于在桌面上初始播放视频的视频比特率（以千比特/秒或kbps为单位）。 </p> <p>如果自适应视频集中不存在此比特率值，则视频播放器会启动比特率最低的视频。 </p> <p>如果设置为 <span class="codeph"> 0 </span>，则视频播放器将从尽可能低的比特率开始。 仅适用于不支持HTML5 HLS视频（在Windows 10上为Firefox、Chrome和Internet Explorer 11浏览器）的本机系统，以及将播放模式设置为 <span class="codeph"> 自动 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
