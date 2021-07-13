---
description: 视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.mutevolume
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: Developer,User
exl-id: 8f644a40-7fd9-4edd-be29-698635b46507
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

视频查看器的配置属性。

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 在初始加载时设置视频播放的静音模式。 如果设置为<span class="codeph"> 1 </span>，则卷将静音；否则，视频将播放声音。 在某些在加载时导致视频播放延迟的设备上，还允许视频自动播放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
