---
description: 'null'
seo-description: 'null'
seo-title: 色板。启用拖动
solution: Experience Manager
title: 色板。启用拖动
topic: Dynamic media
uuid: fbff46d7-f947-40ae-9a0c-7d2496a343f6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 色板。启用拖动{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> 启用或禁用用户使用鼠标或使用触控手势滚动色板的功能 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span></span> </p> </td> 
   <td> <p> 在0- <span class="codeph"> 1范围内的函 </span> 数。 它是一个 <span class="codeph"> %值， </span> 用于在实际速度的错误方向上移动。 如果设置为 <span class="codeph"> 1, </span>则它随鼠标移动。 如果设置为 <span class="codeph"> 0 </span>，则完全不会让您向错误的方向移动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
