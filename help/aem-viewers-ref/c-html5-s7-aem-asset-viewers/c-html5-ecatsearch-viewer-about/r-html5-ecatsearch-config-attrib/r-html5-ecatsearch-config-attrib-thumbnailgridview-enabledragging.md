---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
uuid: 31575fa3-8cc4-468e-b590-77edc3b148d4
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 启用或禁用用户使用鼠标或使用触控手势滚动色板的功能 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> 在<span class="codeph"> 0-1 </span>范围内的函数。 它是一个<span class="codeph"> % </span>值，用于沿实际速度的错误方向移动。 如果设置为<span class="codeph"> 1 </span>，则它随鼠标移动。 如果它设置为<span class="codeph"> 0 </span>，则它不会让您向错误的方向移动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-831c23dea82449bfa50fd155bea365b7}

可选。

## 默认 {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## 示例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
