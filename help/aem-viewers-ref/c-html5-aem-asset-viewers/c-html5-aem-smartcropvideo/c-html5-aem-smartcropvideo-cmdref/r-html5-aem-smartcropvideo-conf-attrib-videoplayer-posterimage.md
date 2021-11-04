---
title: SmartCropVideoPlayer.posterimage
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

智能裁剪视频查看器的配置属性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 要在视频开始播放之前显示在第一帧的图像，针对 <span class="codeph"> serverurl</span>. 如果在URL中指定，则对以下内容进行HTTP编码： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果 <span class="codeph"><span class="varname"> image_id</span></span> 值时，组件会尝试将默认的海报图像改为该资产。 </p> <p>当视频指定为路径时，默认的海报图像目录id将从视频路径派生为 <span class="codeph"> catalog_id/image_id</span> 配对。 的 <span class="codeph"> catalog_id</span> 对应于路径中的第一个令牌和 <span class="codeph"> image_id</span> 是删除了扩展名的视频名称。 如果具有该ID的图像不存在，则不会显示海报图像。 </p> <p>要阻止显示默认海报图像，请指定 <span class="codeph"> 无</span> 作为海报图像值。 如果仅 <span class="codeph"><span class="varname"> isCommands</span></span> ，则在显示图像之前，会将命令应用于默认海报图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
