---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
topic: Dynamic Media
uuid: 0bfd7275-59c7-446f-b056-93ed79352462
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---


# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 启用或禁用用户使用鼠标或触控手势滚动样本的功能 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> 在<span class="codeph"> 0-1 </span>范围内的函数。 它是一个<span class="codeph"> % </span>值，用于沿实际速度的错误方向移动。 如果它设置为<span class="codeph"> 1 </span>，则它随鼠标移动。 如果它设置为<span class="codeph"> 0 </span>，则它不允许您向错误的方向移动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
