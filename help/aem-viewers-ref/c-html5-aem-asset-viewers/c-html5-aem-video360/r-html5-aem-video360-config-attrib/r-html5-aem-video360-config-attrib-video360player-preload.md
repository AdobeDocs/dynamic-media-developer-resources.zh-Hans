---
description: 指示查看器是否在播放开始之前开始加载视频内容。
seo-description: 指示查看器是否在播放开始之前开始加载视频内容。
seo-title: Video360Player.preload
solution: Experience Manager
title: Video360Player.preload
uuid: 6e3b95b8-d585-4164-8665-6211000689fe
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

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
