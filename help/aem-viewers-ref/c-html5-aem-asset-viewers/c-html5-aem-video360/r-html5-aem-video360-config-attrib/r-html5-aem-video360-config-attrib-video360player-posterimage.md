---
description: Video360查看器的配置属性。
solution: Experience Manager
title: Video360Player.posterimage
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---


# Video360Player.posterimage{#video-player-posterimage}

Video360查看器的配置属性。

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制海报图像外观的图像服务修饰符。 如果在URL中指定，则使用HTTP编码： </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> 作 <span class="codeph"> 为%3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> 此修饰符适用于Dynamic Media Classic或AEM Dynamic Media上托管的视频内容。 </p> <p>要阻止显示默认海报图像，请指定<span class="codeph"> none</span>作为海报图像值。 </p> </td> 
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

