---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 6ae18f94-7a0f-429e-9684-eff43f523b1d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`超量拖动值`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 启用或禁用用户使用鼠标或使用触控手势滚动样本的功能 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> 超量拖动值 </span> </span> </p> </td> 
   <td> <p> 函数 <span class="codeph"> 0-1 </span> 范围。 是 <span class="codeph"> % </span> 值。 如果将其设置为 <span class="codeph"> 1 </span>，则会随鼠标移动。 如果将其设置为 <span class="codeph"> 0 </span>，它根本不会让你走错方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
