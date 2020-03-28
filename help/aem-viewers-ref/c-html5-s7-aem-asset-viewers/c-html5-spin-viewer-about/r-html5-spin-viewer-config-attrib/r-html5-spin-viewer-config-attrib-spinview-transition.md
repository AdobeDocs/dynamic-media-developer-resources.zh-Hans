---
description: 'null'
seo-description: 'null'
seo-title: SpinView.过渡
solution: Experience Manager
title: SpinView.过渡
topic: Dynamic media
uuid: 9d7ea421-9892-4276-8f22-3e1099f91f2f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.过渡{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`调`*[, *`整`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定单个缩放步骤操作的动画所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 放松</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速幻觉，使过渡看起来更自然。 可以将放松设置为以下任一选项： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自动） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（线性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2（二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3（立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四分） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（5次） </li> 
     </ul> </p> <p>在禁用弹性缩放时，自动模式始终使用线性过渡（默认）。 否则，它将基于过渡时间适合其他放松功能之一。 即，过渡时间越短，使用放松功能加速加速或减速效果越高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选。

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
