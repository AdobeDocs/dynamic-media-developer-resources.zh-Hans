---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 0b0a88a0-d736-4ab8-a25f-15d1689b0a48
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`持续时间`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> 指定在资源更改时应用于主视图的效果的类型。 <span class="codeph"> none</span>表示无过渡，主视图更改会立即发生。 <span class="codeph"> fade</span>将激活旧图像淡出和新图像淡入的交叉淡入淡出过渡 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">持续时间</span></span> </p> </td> 
   <td colname="col2"> <p> 完成动画所需的秒数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

无。

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`frametransition=fade,1`
