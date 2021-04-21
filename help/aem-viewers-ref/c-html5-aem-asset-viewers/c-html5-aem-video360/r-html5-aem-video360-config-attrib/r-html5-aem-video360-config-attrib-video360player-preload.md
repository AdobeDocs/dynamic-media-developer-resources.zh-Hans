---
description: 指示查看器是否在播放开始之前开始加载视频内容。
solution: Experience Manager
title: Video360Player.preload
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 6%

---

# Video360Player.preload{#video-player-preload}

指示查看器是否在播放开始之前开始加载视频内容。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果设置为<span class="codeph"> 1 </span>，则在设置资产后，视频会立即开始下载；否则，仅在最终用户或API调用启动播放后预载开始。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则某些功能在播放开始前可能无法使用；具体而言，搜索操作不会更新视频帧。 如果禁用海报图像，则查看器将显示为空区域，而不是第一个视频帧。 </p> <p>请注意，在某些版本的Internet Explorer 11和Edge浏览器上，可能会忽略禁用视频预载。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
