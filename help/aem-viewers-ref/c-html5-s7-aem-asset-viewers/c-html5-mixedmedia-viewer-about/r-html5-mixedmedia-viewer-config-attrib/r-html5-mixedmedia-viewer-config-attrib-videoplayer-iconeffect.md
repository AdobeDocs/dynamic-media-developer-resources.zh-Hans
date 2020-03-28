---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 8e112f3c-8fa6-4c77-94c5-5027275225e7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1countfadeauto`*[, *``*][, *``*][, *`隐藏`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 使IconEffect在视频暂停时显示在视频顶部。 在某些设备上使用本机控件。 在这种情况下，将忽 <span class="codeph"> 略iconeffect修饰符</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect显示和重新显示的最大次数。 值为-1 <span class="codeph"> 表示</span> ，该图标将无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡入淡出</span></span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自 <span class="varname"> 动隐藏</span></span> </p> </td> 
   <td colname="col2"> <p> 设置IconEffect在自动隐藏前保持可见的秒数。 即，淡入动画之后和淡出动画开始之前的时间。 设置为 <span class="codeph"> 0</span> 将禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
