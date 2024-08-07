---
title: 缩放模式
description: 设置缩放交互的类型。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# 缩放模式{#zoommode}

设置缩放交互的类型。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">连续|内联|自动</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuous </span>启用经典缩放，即当您在主视图中单击、双击或捏出图像时，图像将逐渐放大。 要返回到初始视图，请缩小或重置缩放状态。 类 </p> <p> <span class="codeph">内联</span>启用即时缩放，当您将主视图悬停在桌面上或触摸并按住触摸设备时，缩放的图像会立即显示。 从视图中移动鼠标或松开手指后，图像会自动恢复到初始状态。 在<span class="codeph">内联</span>模式下，嵌套图像集将被扁平化并显示为单个缩略图。 类<span class="codeph">自动</span>在桌面上激活内联模式，在触控设备上激活连续模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
