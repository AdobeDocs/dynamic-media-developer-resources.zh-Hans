---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic Media
uuid: 9eab6cb2-92a3-41d2-999a-254a7109d6b6
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

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

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
