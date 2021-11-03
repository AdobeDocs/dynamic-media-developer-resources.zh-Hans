---
description: 指示查看器是否在播放开始之前开始加载视频内容。
solution: Experience Manager
title: SmartCropVideoPlayer.preload
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

指示查看器是否在播放开始之前开始加载视频内容。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果设置为 <span class="codeph"> 1 </span> 资产设置后，视频即开始下载；否则，仅在最终用户或API调用启动播放后，才会开始预加载。 </p> <p>如果设置为 <span class="codeph"> 0 </span> 某些功能可能在播放开始后才能正常工作；具体而言，搜寻操作不会更新视频帧。 如果禁用了海报图像，则查看器将显示为空区域，而不是第一个视频帧。 </p> <p>请注意，在Internet Explorer 11和Edge浏览器的某些版本上，可能会忽略禁用视频预加载的操作。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
