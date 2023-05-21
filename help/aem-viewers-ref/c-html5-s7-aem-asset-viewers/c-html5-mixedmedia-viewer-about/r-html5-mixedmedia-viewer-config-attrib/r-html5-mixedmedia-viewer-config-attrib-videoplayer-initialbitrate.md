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
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`值`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
   <td colname="col2"> <p>設定在桌上型電腦上初始播放視訊所使用的視訊位元速率（以千位元/秒或kbps為單位）。 </p> <p>如果此位元速率值不存在最適化視訊集中，則視訊播放器會啟動具有下一個最低位元速率的視訊。 </p> <p>若設為 <span class="codeph"> 0 </span>，視訊播放器會從最低的位元速率開始。 僅適用於對HTML5 HLS視訊沒有原生支援的系統（Windows 10上的Firefox、Chrome和Internet Explorer 11瀏覽器），且播放模式設定為時 <span class="codeph"> 自動 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
