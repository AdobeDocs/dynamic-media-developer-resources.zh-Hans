---
title: 缩放模式
description: 设置缩放交互的类型。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
TQID: 'https://experienceleague.adobe.com/Joa1KBx6spGvXsMkjxSCPn-23cICUffLJ9CWOQ-BRwo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
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
