---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持续时间`*[, *`计数`*][, *`渐隐`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>指定提示文本在隐藏之前显示的秒数。 当设置为<span class="codeph"> -1</span>时，即使用户激活弹出窗口，也会始终显示消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">计数</span> </span> </p> </td> 
   <td colname="col2"> <p>指定查看集中的新图像时文本显示的次数。 值为<span class="codeph"> -1</span>表示在查看集中的任何图像时始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">淡化</span> </span> </p> </td> 
   <td colname="col2"> <p>指定文本出现或消失时出现的渐隐动画的持续时间。 值为<span class="codeph"> 0</span>表示没有渐隐过渡。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
