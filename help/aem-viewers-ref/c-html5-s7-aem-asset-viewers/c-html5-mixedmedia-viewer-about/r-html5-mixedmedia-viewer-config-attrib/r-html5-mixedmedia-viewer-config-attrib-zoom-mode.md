---
description: 设置缩放交互的类型。
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# zoomMode{#zoommode}

设置缩放交互的类型。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 连续|内联|自动  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 连续 </span> 可启用经典缩放功能，在主视图中，当您单击、双击或收缩图像时，图像会逐渐放大。您需要显式缩小或重置缩放状态才能返回到初始视图。 </p> <p> <span class="codeph"> 内联 </span> 可实现即时缩放，当您将鼠标悬停在桌面上的主视图上或触摸并按住触控设备时，缩放的图像会立即显示；当您从视图中移动鼠标或松开手指时，图像会自动还原为初始状态。请注意，在内联</span>模式下，嵌套图像集会被扁平化，并显示为单个缩略图。 <span class="codeph"><span class="codeph"> 自动 </span> 在桌面上激活内联模式，在触控设备上激活连续模式。 </span></p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
