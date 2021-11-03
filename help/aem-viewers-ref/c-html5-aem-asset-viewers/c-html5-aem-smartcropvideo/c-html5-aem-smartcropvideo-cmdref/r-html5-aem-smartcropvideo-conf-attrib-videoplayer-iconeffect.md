---
title: SmartCropVideoPlayer.iconeffect
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

智能裁剪视频查看器的配置属性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`计数`*][, *`淡淡`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 在视频暂停时，使IconEffect能够显示在视频顶部。 在某些设备上，使用本机控件。 在这种情况下， <span class="codeph"> iconeft</span> 修饰符被忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出现和重新出现的最大次数。 值 <span class="codeph"> -1</span> 指示图标无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡淡</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> 设置IconEffect在自动隐藏之前保持可见的秒数。 即，淡入动画完成后和淡出动画开始前的时间。 设置 <span class="codeph"> 0</span> 禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
