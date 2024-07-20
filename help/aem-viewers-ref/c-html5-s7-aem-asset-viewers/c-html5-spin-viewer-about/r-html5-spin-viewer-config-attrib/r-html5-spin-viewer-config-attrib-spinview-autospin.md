---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`持续时间`*][, *`方向`*][, *`旋转数`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 启用或禁用自动旋转动画。 要获得最佳的自动旋转体验，建议通过将<span class="codeph"> maxloadradius</span>设置为<span class="codeph"> -1</span>来预加载所有帧。 但请注意，此设置会增加加载时间和带宽使用量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">持续时间</span></span> </p> </td> 
   <td colname="col2"> <p> 每个完整旋转的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">方向</span></span> </p> </td> 
   <td colname="col2"> <p> 旋转方向为<span class="codeph"> 0</span>（向东旋转）和<span class="codeph"> 1</span>（向西旋转）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">旋转数</span></span> </p> </td> 
   <td colname="col2"> <p> 自动旋转停止前完成的完整旋转次数。 该数字为浮点数。 设置为<span class="codeph"> -1</span>可实现无限自动旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
