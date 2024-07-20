---
title: VideoPlayer.iconeffect
description: 视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`计数`*][, *`渐隐`*][, *`自动隐藏`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 启用IconEffect以在视频暂停时在视频顶部显示。 在某些设备上，使用本机控件。 在这种情况下，将忽略<span class="codeph"> iconeffect</span>修饰符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">计数</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出现和重新出现的最大次数。 值为<span class="codeph"> -1</span>表示该图标将无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">淡化</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">自动隐藏</span> </span> </p> </td> 
   <td colname="col2"> <p> 设置IconEffect在自动隐藏之前保持可见状态的秒数。 即，淡入动画完成之后和淡出动画开始之前的时间。 设置为<span class="codeph"> 0</span>可禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
