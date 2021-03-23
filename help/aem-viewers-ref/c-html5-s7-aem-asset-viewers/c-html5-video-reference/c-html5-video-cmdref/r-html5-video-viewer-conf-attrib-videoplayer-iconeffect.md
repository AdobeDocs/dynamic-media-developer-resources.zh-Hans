---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 当视频暂停时，启用IconEffect以在视频顶部显示。 在某些设备上使用本机控件。 在这种情况下，将忽略<span class="codeph"> iconeffect</span>修饰符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect显示和重新显示的最大次数。 值<span class="codeph"> -1</span>表示图标无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡入</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 自动隐藏</span> </span> </p> </td> 
   <td colname="col2"> <p> 设置IconEffect在自动隐藏前保持可见的秒数。 即，淡入动画完成后的时间和淡出动画开始之前的时间。 设置<span class="codeph"> 0</span>将禁用自动隐藏行为。 </p> </td> 
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

