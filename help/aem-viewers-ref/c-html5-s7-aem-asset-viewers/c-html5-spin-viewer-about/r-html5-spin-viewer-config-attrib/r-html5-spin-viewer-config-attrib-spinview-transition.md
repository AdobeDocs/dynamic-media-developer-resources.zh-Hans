---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: Developer,User
exl-id: 85dbd5cd-b212-4c77-8f5a-ffbdaca27fdb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 4%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`调整`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定动画执行单个缩放步骤操作所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 宽松</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速的假象，使过渡更自然。 您可以将缓动设置为以下任一值： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自动） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（线性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2（二次方） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3（立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四分） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（五度） </li> 
     </ul> </p> <p>禁用弹性缩放时，自动模式始终使用线性过渡（默认）。 否则，它将适合基于过渡时间的其他缓动功能之一。 即过渡时间越短，用缓动函数加速或减速效果越大。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选。

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
