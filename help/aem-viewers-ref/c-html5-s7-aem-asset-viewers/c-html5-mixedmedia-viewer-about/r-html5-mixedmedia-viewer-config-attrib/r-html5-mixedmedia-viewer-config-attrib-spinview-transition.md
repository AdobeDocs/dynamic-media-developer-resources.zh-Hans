---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`时间`*[, *`宽松`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定动画执行单个缩放步骤操作所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 宽松</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速的假象，使过渡更自然。 您可以将缓动设置为以下任一值： </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0（自动） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1（线性） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2（二次方） </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3（立方） </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4（四分） </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5（五度） </li> 
     </ul> </p> <p>禁用弹性缩放时，自动模式始终使用线性过渡（默认）。 否则，它将适合基于过渡时间的其他缓动功能之一。 即过渡时间越短，用缓动函数加速或减速效果越大。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
