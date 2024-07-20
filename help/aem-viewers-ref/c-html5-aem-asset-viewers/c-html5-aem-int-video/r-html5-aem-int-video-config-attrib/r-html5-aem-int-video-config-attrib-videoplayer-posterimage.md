---
title: VideoPlayer.posterimage
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 17c1220d-f2a4-4729-84e2-b9f6f5732423
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">无|[<span class="varname"> image_id</span>][？<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 在视频开始播放前的第一帧显示的图像，已针对<span class="codeph"> serverurl</span>进行解析。 如果在URL中指定，则对以下内容进行HTTP编码： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph">？</span>作为<span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span>作为<span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span>作为<span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果忽略<span class="codeph"><span class="varname"> image_id</span></span>值，则组件会尝试为该资源使用默认的海报图像。 </p> <p>将视频指定为路径时，默认海报图像目录ID派生自视频路径，作为<span class="codeph"> catalog_id/image_id</span>对，其中<span class="codeph"> catalog_id</span>对应于路径中的第一个令牌。 并且，<span class="codeph"> image_id</span>是删除了扩展的视频的名称。 如果该ID的图像不存在，则不会显示海报图像。 </p> <p>要阻止显示默认海报图像，请将<span class="codeph"> none</span>指定为海报图像值。 如果只指定了<span class="codeph"><span class="varname"> isCommands</span></span>，则在显示图像之前将命令应用于默认海报图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
