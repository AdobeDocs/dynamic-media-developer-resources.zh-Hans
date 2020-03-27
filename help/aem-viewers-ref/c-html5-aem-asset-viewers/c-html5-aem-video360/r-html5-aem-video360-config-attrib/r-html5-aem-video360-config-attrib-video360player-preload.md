---
description: 指示查看器是否在播放开始之前开始加载视频内容。
seo-description: 指示查看器是否在播放开始之前开始加载视频内容。
seo-title: Video360Player.preload
solution: Experience Manager
title: Video360Player.preload
topic: Dynamic media
uuid: 6e3b95b8-d585-4164-8665-6211000689fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.preload{#video-player-preload}

指示查看器是否在播放开始之前开始加载视频内容。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 如果设置为 <span class="codeph"> 1, </span> 则视频在资产设置完成后立即开始下载；否则，仅在最终用户或API调用启动播放后预载开始。 </p> <p>如果设置为 <span class="codeph"> 0, </span> 某些特性在播放开始后才能工作；具体而言，搜索操作不会更新视频帧。 如果海报图像被禁用，则查看器将显示为空区域而不是第一个视频帧。 </p> <p>请注意，在某些版本的Internet Explorer 11和Edge浏览器上禁用视频预载可能会被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
