---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`计数`*][, *`渐隐`*][, *`自动隐藏`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 启用IconEffect以在图像处于重置状态时显示在图像顶部，这表示有可与图像交互的可用操作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">计数</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出现和重新出现的最大次数。 值为<span class="codeph"> -1</span>表示该图标将始终无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">淡化</span> </span> </p> </td> 
   <td colname="col2"> <p>指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">自动隐藏</span> </span> </p> </td> 
   <td colname="col2"> <p>设置IconEffect在自动隐藏之前保持完全可见的秒数。 即，淡入动画完成之后、淡出动画开始之前的时间。 设置为<span class="codeph"> 0</span>可禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-50bcd15223174bb79ce08b31ea03d682}

可选.

## 默认 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## 示例 {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
