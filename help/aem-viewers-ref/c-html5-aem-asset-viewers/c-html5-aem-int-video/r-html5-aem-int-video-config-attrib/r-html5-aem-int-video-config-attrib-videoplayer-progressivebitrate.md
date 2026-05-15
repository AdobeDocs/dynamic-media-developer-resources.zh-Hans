---
title: VideoPlayer.progressivebitrate
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
TQID: 'https://experienceleague.adobe.com/FKD3lPjlXUFjmtI8Zb9u0nrWlDa8B4wxqLOkqok6Vok'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`值`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">值</span> </p> </td> 
   <td colname="col2"> <p> 指定当前系统不支持自适应视频播放时，在自适应视频集中播放视频所需的视频比特率(以千位/秒(kbps)为单位)。 </p> <p>组件将选取比特率最接近（但不超过）指定值的视频流。 如果自适应视频集中的所有视频流都具有高于指定值的质量，则逻辑会选择具有最低质量的比特率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 示例： {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
