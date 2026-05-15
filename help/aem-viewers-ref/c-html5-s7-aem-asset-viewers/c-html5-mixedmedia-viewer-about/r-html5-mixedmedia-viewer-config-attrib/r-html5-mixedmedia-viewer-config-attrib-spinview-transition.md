---
title: 旋转视图。过渡
description: 旋转视图。过渡
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
TQID: 'https://experienceleague.adobe.com/8v0KA79kf8-EGxgxxJ4FfldLCzUh5wAiV0dy4LmcM5A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# 旋转视图。过渡{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`次`*[, *`缓动`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">次</span></span> </p> </td> 
   <td colname="col2"> <p> 指定单个缩放步长操作的动画所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">缓动</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速的假象，使过渡更加自然。 可以将缓动设置为下列操作之一： </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0（自动） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1（线性） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 （二次） </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 （立方） </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4（四次） </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5（五次） </li> 
     </ul> </p> <p>禁用弹性缩放（默认）时，自动模式始终使用线性过渡。 否则，它会根据过渡时间调整其他缓动功能之一。 即过渡时间越短，缓动函数用于加速加速或减速效果的效果越好。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
