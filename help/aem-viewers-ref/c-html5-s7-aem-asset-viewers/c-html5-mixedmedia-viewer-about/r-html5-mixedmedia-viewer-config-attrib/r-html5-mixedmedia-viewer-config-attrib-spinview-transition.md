---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
topic: Dynamic Media
uuid: d5cc319a-fb0b-41d3-a118-f00376a127e4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`调`*[, *`整`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定单个缩放步骤操作的动画所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 放松</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速幻觉，使过渡更自然。 可以将放松设置为以下任一设置： </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0（自动） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1（线性） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2（二次） </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3（立方） </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4（四分） </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5（五次） </li> 
     </ul> </p> <p>禁用弹性缩放时，自动模式始终使用线性过渡（默认）。 否则，它将适合基于过渡时间的其他放松功能之一。 即，过渡时间越短，使用放松功能加速加速或减速效果的时间越高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
