---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
uuid: 38350e3d-515b-454c-bc85-39b91ad06e8b
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 当图像处于重置状态时，使IconEffect能够显示在图像的顶部，并提示可用操作与图像交互。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect显示和重新显示的最大次数。 值<span class="codeph"> -1</span>表示图标始终无限地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡入</span> </span> </p> </td> 
   <td colname="col2"> <p>指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 自动隐藏</span> </span> </p> </td> 
   <td colname="col2"> <p>设置IconEffect在自动隐藏前保持完全可见的秒数。 即，淡入动画完成后但淡出动画开始之前的时间。 设置<span class="codeph"> 0</span>将禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-50bcd15223174bb79ce08b31ea03d682}

可选。

## 默认 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## 示例 {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
