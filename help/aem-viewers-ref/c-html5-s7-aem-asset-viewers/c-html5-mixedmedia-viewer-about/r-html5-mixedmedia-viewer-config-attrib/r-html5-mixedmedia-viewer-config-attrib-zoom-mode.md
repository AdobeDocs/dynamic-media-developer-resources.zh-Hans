---
description: 设置缩放交互的类型。
seo-description: 设置缩放交互的类型。
seo-title: zoomMode
solution: Experience Manager
title: zoomMode
topic: Dynamic media
uuid: fdbe7ab6-47db-46cf-8a0d-085c66d4b0f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# zoomMode{#zoommode}

设置缩放交互的类型。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 连续|内联|自动 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 连续 </span> 功能支持经典缩放，在主视图中单击、多次点按或捏合时，图像会逐渐放大。 您需要显式缩小或重置缩放状态，才能返回到初始视图。 </p> <p> <span class="codeph"> 内联 </span> 支持即时缩放，当您将主视图悬停在桌面上或在触控设备上触控和按住鼠标时，缩放后的图像会立即显示；当您从视图中移动鼠标或松开手指时，图像会自动恢复到初始状态。 请注意，在内联 <span class="codeph"> 模式 </span> 中，嵌套图像集是平展的，并显示为单个缩略图。 <span class="codeph"> 自动 </span> 激活桌面上的内联模式和触控设备上的连续模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
