---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 011ef772-6760-4794-819e-2a822fbae1b5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 啟用或停用使用者利用滑鼠或觸控手勢捲動色票的能力 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> 中的函式 <span class="codeph"> 0-1 </span> 範圍。 它是 <span class="codeph"> % </span> 以實際速度在錯誤方向移動的值。 如果設定為 <span class="codeph"> 1 </span>，它會隨滑鼠移動。 如果設定為 <span class="codeph"> 0 </span>，讓您完全無法向錯誤的方向移動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-831c23dea82449bfa50fd155bea365b7}

可选.

## 默认 {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## 示例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
