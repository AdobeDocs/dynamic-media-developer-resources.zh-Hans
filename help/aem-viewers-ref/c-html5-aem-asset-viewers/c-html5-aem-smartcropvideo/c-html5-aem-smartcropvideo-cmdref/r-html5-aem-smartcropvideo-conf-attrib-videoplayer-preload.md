---
title: SmartCropVideoPlayer.preload
description: 指示查看器是否在开始播放之前开始加载视频内容。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

指示查看器是否在开始播放之前开始加载视频内容。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 如果设置为<span class="codeph"> 1 </span>，则在设置资源后开始下载视频；否则，仅在最终用户或API调用启动播放后开始预加载。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则在再次开始播放之前，某些功能可能无法工作；具体而言，搜寻操作不会更新视频帧。 如果禁用了海报图像，则查看器将显示为空区域，而不是第一个视频帧。 </p> <p>在某些版本的Internet Explorer 11和Edge浏览器上，禁用视频预加载可能会被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
