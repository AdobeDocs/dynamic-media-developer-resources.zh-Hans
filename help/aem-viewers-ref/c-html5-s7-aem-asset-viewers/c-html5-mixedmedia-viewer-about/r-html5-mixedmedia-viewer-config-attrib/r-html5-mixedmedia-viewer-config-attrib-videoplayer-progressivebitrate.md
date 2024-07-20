---
title: VideoPlayer.progressivebitrate
description: VideoPlayer.progressivebitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: b156d3f4-c4d3-45fe-b3d3-b7ed38f6eb4d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`值`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">值</span></span> </p> </td> 
   <td colname="col2"> <p> 指定当前系统不支持自适应视频播放时，在自适应视频集中播放视频所需的视频比特率（以千位/秒或kbps为单位）。 </p> <p>组件将选取比特率最接近（但不超过）指定值的视频流。 如果自适应视频集中的所有视频流都具有高于指定值的品质，则逻辑会选择品质最低的比特率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
