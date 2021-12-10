---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '75'
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
   <td> <p> <span class="codeph"> <span class="varname"> 超量拖动值 </span> </span> </p> </td> 
   <td> <p> 函数 <span class="codeph"> 0-1 </span> 范围。 是 <span class="codeph"> % </span> 值。 如果将其设置为 <span class="codeph"> 1 </span>，则会随鼠标移动。 如果将其设置为 <span class="codeph"> 0 </span>，它根本不会让你走错方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-831c23dea82449bfa50fd155bea365b7}

可选。

## 默认 {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## 示例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
