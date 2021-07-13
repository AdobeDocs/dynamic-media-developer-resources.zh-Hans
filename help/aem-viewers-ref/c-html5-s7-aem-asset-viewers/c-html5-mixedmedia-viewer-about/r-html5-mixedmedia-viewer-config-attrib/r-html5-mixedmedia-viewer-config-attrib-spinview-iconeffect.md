---
description: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,User
exl-id: 473207d2-7e26-4ea3-940e-5a21f29a2b91
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_DF2137DF9C7441B381D2B03CEE4B880A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 当图像处于重置状态时，允许<span class="codeph"> iconeffect</span>在图像顶部显示，并提示可以执行与图像交互的操作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定<span class="codeph"> iconeffect</span>出现和重新显示的最大次数。 值<span class="codeph"> -1</span>表示图标始终无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡淡</span></span> </p> </td> 
   <td colname="col2"> <p>指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>设置<span class="codeph"> iconeffect</span>在自动隐藏之前保持完全可见的秒数。 即，淡入动画完成后但在淡出动画开始之前的时间。 设置<span class="codeph"> 0</span>将禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
