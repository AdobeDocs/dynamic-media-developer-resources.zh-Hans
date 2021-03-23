---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
uuid: c85ad85f-a802-4f5d-9046-00171ad2d9ca
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 4%

---


# PageView.transition{#pageview-transition}

[!DNL `[PageView.|<containerId>_pageView.]transition= *`调`*[, *`整`*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定单个缩放步骤操作的动画所花费的时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 放松</span></span> </p> </td> 
   <td colname="col2"> <p> 创建加速或减速幻觉，使过渡更自然。 可以将放松设置为以下任一选项： </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0（自动） </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1（线性） </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2（二次） </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3（立方） </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4（四分） </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5（五次） </li> 
     </ul> </p> <p>禁用弹性缩放时，自动模式始终使用线性过渡（默认）。 否则，它将适合基于过渡时间的其他缓动功能之一。 即，过渡时间越短，使用缓动功能加速或减速效果的时间越高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ebfd9162c8504666bf0e4485bf3b1383}

可选。

## 默认 {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## 示例 {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`]
