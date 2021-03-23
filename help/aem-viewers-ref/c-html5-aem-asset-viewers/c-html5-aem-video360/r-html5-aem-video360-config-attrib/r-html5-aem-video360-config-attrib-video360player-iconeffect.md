---
description: Video360查看器的配置属性。
seo-description: Video360查看器的配置属性。
seo-title: Video360Player.iconeffect
solution: Experience Manager
title: Video360Player.iconeffect
uuid: a0a2f840-e330-4636-8daf-1cd3f2eddf01
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 8%

---


# Video360Player.iconeffect{#video-player-iconeffect}

Video360查看器的配置属性。

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

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
