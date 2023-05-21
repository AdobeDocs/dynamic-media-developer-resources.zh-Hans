---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 85dbd5cd-b212-4c77-8f5a-ffbdaca27fdb
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`時間`*[, *`加/減速`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單一縮放步階動作動畫所需的時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 加/減速</span></span> </p> </td> 
   <td colname="col2"> <p> 建立加速或減速的錯覺，使轉接看起來更自然。 您可以將加/減速設定為下列其中一個： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 （自動） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 （線性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 （二次方程式） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 （立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 （四次方） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 （五次方） </li> 
     </ul> </p> <p>當彈性縮放被停用（預設）時，「自動」模式一律使用線性轉換。 否則，它會根據轉接時間來配合其他加/減速功能之一。 也就是說，轉接時間越短，使用加/減速功能來加速加速加速或減速效果的速度就越高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
