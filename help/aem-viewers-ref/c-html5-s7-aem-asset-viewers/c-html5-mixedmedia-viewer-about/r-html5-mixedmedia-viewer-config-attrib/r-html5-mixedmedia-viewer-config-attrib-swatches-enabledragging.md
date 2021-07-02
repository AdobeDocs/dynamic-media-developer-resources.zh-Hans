---
description: Swatches.enabledragging
solution: Experience Manager
title: Swatches.enabledragging
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: fd432573-677f-4c46-9cc1-88089496ce75
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

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
   <td> <p> <span class="codeph"> <span class="varname"> 超量拖动值  </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span>范围内的函数。 它是一个<span class="codeph"> % </span>值，用于在实际速度的错误方向上移动。 如果将其设置为<span class="codeph"> 1 </span>，则会随鼠标移动。 如果将其设置为<span class="codeph"> 0 </span>，则完全不允许您沿错误的方向移动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
