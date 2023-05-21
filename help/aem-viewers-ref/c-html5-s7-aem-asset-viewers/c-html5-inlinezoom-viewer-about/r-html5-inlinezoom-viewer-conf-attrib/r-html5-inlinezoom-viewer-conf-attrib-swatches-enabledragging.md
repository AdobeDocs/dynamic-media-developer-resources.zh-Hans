---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 9b69f6d7-b7a1-42c6-98d7-80952b7f8b31
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

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

## 屬性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
