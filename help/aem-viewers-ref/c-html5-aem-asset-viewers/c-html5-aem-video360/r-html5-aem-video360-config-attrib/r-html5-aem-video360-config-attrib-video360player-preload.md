---
title: Video360Player.preload
description: 指示查看器是否在播放开始之前开始加载视频内容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# Video360Player.preload{#video-player-preload}

指示查看器是否在播放开始之前开始加载视频内容。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果设置为 <span class="codeph"> 1 </span>时，会在设置资源后立即开始下载视频。 否则，只有在最终用户或API调用启动播放后，才会开始预加载。 </p> <p>如果设置为 <span class="codeph"> 0 </span>，某些功能在播放开始之前可能无法正常工作。 具体而言，搜寻操作不会更新视频帧。 如果禁用了海报图像，则查看器将显示为空区域，而不是第一个视频帧。 </p> <p>某些版本的Internet Explorer 11和Edge浏览器可能会忽略禁用视频预加载。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
