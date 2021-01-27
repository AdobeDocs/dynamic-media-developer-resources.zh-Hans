---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition
topic: Dynamic Media
uuid: c9cd5df1-fb7b-4acb-afc1-a62b563d8654
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---


# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`时段`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|淡入淡出</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> 指定在资产更改时应用于主视图的效果类型。 </p> <p><span class="codeph"> 不代</span> 表没有过渡，主视图更改会立即发生。 </p> <p><span class="codeph"> 无</span> 法激活交叉淡入淡出过渡，旧图像淡出，新图像淡入淡出 </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 动画完成所需的秒数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

无。

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
