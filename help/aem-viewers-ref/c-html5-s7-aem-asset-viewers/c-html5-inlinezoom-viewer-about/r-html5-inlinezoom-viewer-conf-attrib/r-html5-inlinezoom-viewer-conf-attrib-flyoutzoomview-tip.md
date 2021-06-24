---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: Developer,Business Practitioner
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>指定提示文本在隐藏之前显示的秒数。 如果设置为<span class="codeph"> -1</span>，则始终会显示消息，即使用户激活弹出窗口也是如此。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span> </span> </p> </td> 
   <td colname="col2"> <p>指定在查看集合中的新图像时显示文本的次数。 值<span class="codeph"> -1</span>表示在查看集合中的任何图像时始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡淡</span> </span> </p> </td> 
   <td colname="col2"> <p>指定文本出现或消失时出现的渐隐动画的持续时间。 值<span class="codeph"> 0</span>表示没有渐隐过渡。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
