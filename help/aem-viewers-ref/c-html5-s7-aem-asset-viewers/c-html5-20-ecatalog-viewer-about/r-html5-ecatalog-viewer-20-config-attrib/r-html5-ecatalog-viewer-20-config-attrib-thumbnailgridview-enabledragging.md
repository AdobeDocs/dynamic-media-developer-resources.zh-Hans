---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`超量拖动值`*]`

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

## 属性 {#section-831c23dea82449bfa50fd155bea365b7}

可选。

## 默认 {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## 示例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
