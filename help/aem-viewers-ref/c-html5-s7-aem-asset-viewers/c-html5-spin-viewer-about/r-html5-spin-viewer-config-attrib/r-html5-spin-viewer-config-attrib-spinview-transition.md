---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 85dbd5cd-b212-4c77-8f5a-ffbdaca27fdb
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`次`*[, *`缓动`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">次</span></span> </p> </td> 
   <td colname="col2"> <p> 指定单个缩放步长操作的动画所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">缓动</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速的假象，使过渡更加自然。 可以将缓动设置为下列操作之一： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自动） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（线性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 （二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 （立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四次） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（五次） </li> 
     </ul> </p> <p>禁用弹性缩放（默认）时，自动模式始终使用线性过渡。 否则，它会根据过渡时间调整其他缓动功能之一。 即过渡时间越短，缓动函数用于加速加速或减速效果的效果越好。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
