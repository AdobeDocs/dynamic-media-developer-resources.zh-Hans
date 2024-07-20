---
title: VideoPlayer.mutevolume
description: 混合媒体视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 13398ac5-7137-4345-88b8-5e4df09edb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 5%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

混合媒体视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 在初始加载时为视频播放设置静音模式。 如果设置为<span class="codeph"> 1 </span>，则音量将静音；否则，视频将播放声音。 在某些设备上，加载时将视频播放静音还允许视频自动播放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
