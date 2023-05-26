---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e9db5c83-e6cf-4847-99b3-a1cf6a1fbe9f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# PageView.transition{#pageview-transition}

[!DNL `[PageView.|<containerId>_pageView.]transition= *`时间`*[, *`缓动`*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定单个缩放步长操作的动画所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 缓动</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速的假象，使过渡更加自然。 可以将缓动设置为以下任一值： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自动） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（线性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 （二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 （立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四次） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 （五次） </li> 
     </ul> </p> <p>禁用弹性缩放（默认）时，“自动”模式始终使用线性过渡。 否则，它会根据过渡时间调整其他缓动功能之一。 即过渡时间越短，加减速效果越快。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ebfd9162c8504666bf0e4485bf3b1383}

可选.

## 默认 {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## 示例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`]
