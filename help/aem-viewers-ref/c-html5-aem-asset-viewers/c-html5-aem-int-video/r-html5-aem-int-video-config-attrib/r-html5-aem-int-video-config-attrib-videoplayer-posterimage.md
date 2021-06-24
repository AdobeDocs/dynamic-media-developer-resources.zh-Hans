---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,Business Practitioner
exl-id: 17c1220d-f2a4-4729-84e2-b9f6f5732423
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 要在视频开始播放之前在第一帧上显示的图像，针对<span class="codeph"> serverurl</span>进行解析。 如果在URL中指定，则对以下内容进行HTTP编码： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作为 <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>如果忽略<span class="codeph"><span class="varname"> image_id</span></span>值，则组件会尝试为该资产使用默认的海报图像。 </p> <p>将视频指定为路径时，默认的海报图像目录id将从视频路径派生，因为<span class="codeph"> catalog_id/image_id</span>对中<span class="codeph"> catalog_id</span>对应于路径中的第一个令牌，而<span class="codeph"> image_id</span>是扩展名为已删除的视频的名称。 如果具有该ID的图像不存在，则不会显示海报图像。 </p> <p>要阻止显示默认海报图像，请指定<span class="codeph"> none</span>作为海报图像值。 如果仅指定了<span class="codeph"><span class="varname"> isCommands</span></span> ，则在显示图像之前，命令会应用于默认海报图像。 </p> </td> 
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
