---
title: VideoPlayer.preload
description: 指示查看器是否在播放开始之前开始加载视频内容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# VideoPlayer.preload{#videoplayer-preload}

指示查看器是否在播放开始之前开始加载视频内容。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果设置为 <span class="codeph"> 1 </span> 设置资源后，视频就会开始下载；否则，只有在最终用户启动播放或API调用后，才会开始预加载。 </p> <p>如果设置为 <span class="codeph"> 0 </span> 某些功能在播放开始之前可能无法正常工作；具体而言，搜寻操作不会更新视频帧。 如果禁用了海报图像，则查看器将显示为空区域，而不是第一个视频帧。 </p> <p>某些版本的Internet Explorer 11和Edge浏览器可能会忽略禁用视频预加载。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
