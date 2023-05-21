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
ht-degree: 3%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`時間`*[, *`加/減速`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定單一縮放步階動作動畫所需的時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 加/減速</span></span> </p> </td> 
   <td colname="col2"> <p> 建立加速或減速的錯覺，使轉接看起來更自然。 您可以將加/減速設定為下列其中一個： </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 （自動） </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 （線性） </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 （二次方程式） </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 （立方） </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 （四次方） </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 （五次方） </li> 
     </ul> </p> <p>當彈性縮放被停用（預設）時，「自動」模式一律使用線性轉換。 否則，它會根據轉接時間來配合其他加/減速功能之一。 也就是說，轉接時間越短，使用加/減速功能來加速加速加速或減速效果的速度就越高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
