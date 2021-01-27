---
description: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
topic: Dynamic Media
uuid: 1d58d230-f056-4cd8-a36f-b0f5d43483a3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`调`*[, *`整`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定单个缩放步骤操作的动画所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 放松</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速幻觉，使过渡更自然。 可以将放松设置为以下任一设置： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自动） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（线性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2（二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3（立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四分） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（五次） </li> 
     </ul> </p> <p>禁用弹性缩放时，自动模式始终使用线性过渡（默认）。 否则，它将适合基于过渡时间的其他放松功能之一。 即，过渡时间越短，使用放松功能加速加速或减速效果的时间越高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`0.5,0`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`transition=2,2`
