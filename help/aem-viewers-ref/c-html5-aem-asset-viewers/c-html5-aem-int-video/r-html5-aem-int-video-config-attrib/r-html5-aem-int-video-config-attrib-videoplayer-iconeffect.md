---
description: 交互式视频查看器的配置属性。
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

交互式视频查看器的配置属性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 当视频处于暂停状态时，使IconEffect显示在视频顶部。 在某些设备上使用本机控件。 在这种情况下，将忽略<span class="codeph"> iconeffect</span>修饰符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect显示和重新显示的最大次数。 值<span class="codeph"> -1</span>表示图标无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡入</span></span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 自动隐藏</span></span> </p> </td> 
   <td colname="col2"> <p> 设置IconEffect在自动隐藏前保持完全可见的秒数。 即，淡入动画完成之后和淡出动画开始之前的时间。 设置为<span class="codeph"> 0</span>可禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
