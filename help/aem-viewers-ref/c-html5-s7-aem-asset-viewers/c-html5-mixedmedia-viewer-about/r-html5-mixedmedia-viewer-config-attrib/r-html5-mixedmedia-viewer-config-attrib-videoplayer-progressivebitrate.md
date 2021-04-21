---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`值`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 指定在当前系统不支持自适应视频播放时从自适应视频集播放的所需视频比特率（以千位/秒或千位/秒）。 </p> <p>该组件选取最接近（但不超过）指定值的比特率的视频流。 如果自适应视频集中的所有视频流的质量都高于指定值，则逻辑将选择质量最低的比特率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
