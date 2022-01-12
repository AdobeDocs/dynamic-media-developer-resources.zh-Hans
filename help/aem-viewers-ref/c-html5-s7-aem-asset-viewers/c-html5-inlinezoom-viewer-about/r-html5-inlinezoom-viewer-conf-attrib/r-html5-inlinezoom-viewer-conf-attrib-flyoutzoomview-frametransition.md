---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`时段`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|渐隐</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> 指定资产更改时应用于主视图的效果类型。 </p> <p><span class="codeph"> 无</span> 表示没有过渡，主视图更改会立即发生。 </p> <p><span class="codeph"> 淡淡</span> 激活交叉淡入淡出过渡，即旧图像淡出，新图像淡入 </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 动画完成所用的秒数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

无。

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
