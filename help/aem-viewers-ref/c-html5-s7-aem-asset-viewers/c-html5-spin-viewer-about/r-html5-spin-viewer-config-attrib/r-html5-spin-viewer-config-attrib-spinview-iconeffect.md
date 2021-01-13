---
description: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
topic: Dynamic media
uuid: 864fb8dc-34f8-4216-b38c-cc00f7d8d95f
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---


# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 使<span class="codeph"> iconeffect</span>在图像处于重置状态时显示在图像顶部，并提示有可用的操作与图像交互。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定<span class="codeph"> iconeffect</span>出现和重新出现的最大次数。 值<span class="codeph"> -1</span>表示图标始终无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡出</span></span> </p> </td> 
   <td colname="col2"> <p>指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 自动隐藏</span></span> </p> </td> 
   <td colname="col2"> <p>设置在自动隐藏<span class="codeph"> iconeffect</span>之前保持完全可见的秒数。 即，淡入动画完成后但淡出动画开始之前的时间。 设置<span class="codeph"> 0</span>将禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选。

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
