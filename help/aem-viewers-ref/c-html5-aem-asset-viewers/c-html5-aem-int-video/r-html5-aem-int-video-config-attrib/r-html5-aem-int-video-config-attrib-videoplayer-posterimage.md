---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 6b21179c-a227-4194-8640-0fcf73ee80e9
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 播放视频开始之前要在第一帧上显示的图像，已针对serverurl解析 <span class="codeph"> 该图像</span>。 如果在URL中指定，则HTTP编码如下： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作为 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> 作为</span> % <span class="codeph"> 26(&amp;A)</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果忽 <span class="codeph"><span class="varname"> 略image_id值</span></span> ，则组件将尝试为该资产使用默认海报图像。 </p> <p>当视频指定为路径时，默认海报图像目录id从视频路径派生为 <span class="codeph"> catalog_id/image_id</span> 对，其中catalog_id <span class="codeph"> 对应于路径中的第一个令牌，</span><span class="codeph"></span> image_id是删除了扩展名的视频的名称。 如果具有该ID的图像不存在，则不显示海报图像。 </p> <p>要阻止显示默认海报图像，请指定 <span class="codeph"> none</span> 作为海报图像值。 如果仅指 <span class="codeph"><span class="varname"> 定isCommands</span></span> ，则在显示图像之前，命令将应用于默认海报图像。 </p> </td> 
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

