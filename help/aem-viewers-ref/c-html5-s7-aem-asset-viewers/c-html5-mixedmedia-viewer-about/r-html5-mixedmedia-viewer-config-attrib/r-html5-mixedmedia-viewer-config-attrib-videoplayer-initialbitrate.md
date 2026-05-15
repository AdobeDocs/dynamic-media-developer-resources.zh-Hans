---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
TQID: 'https://experienceleague.adobe.com/43fGvsD0G1miDbzE8EQnXmTVrlCQEOP9V2r0ji83yww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
   <td colname="col2"> <p>设置用于在桌面上初始播放视频的视频比特率（以千位/秒或kbps为单位）。 </p> <p>如果此比特率值在自适应视频集中不存在，则视频播放器将启动具有下一个最低比特率的视频。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则视频播放器将从可能的最低比特率开始。 仅适用于对HTML5 HLS视频没有本机支持的系统（Windows 10上的Firefox、Chrome和Internet Explorer 11浏览器），以及播放模式设置为<span class="codeph">自动</span>的情况。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
