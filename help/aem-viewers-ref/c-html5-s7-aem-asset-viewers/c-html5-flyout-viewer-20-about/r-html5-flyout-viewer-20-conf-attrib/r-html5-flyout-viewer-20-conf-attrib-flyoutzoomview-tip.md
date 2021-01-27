---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic Media
uuid: ad423dc7-4dd8-42d9-bf75-db8f309f6aaa
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持续`*[, *``*][, *`衰退`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>指定提示文本在隐藏前显示的秒数。 当设置为<span class="codeph"> -1</span>时，即使用户激活弹出窗口，消息也始终显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span> </span> </p> </td> 
   <td colname="col2"> <p>指定查看集合中的新图像时显示文本的次数。 值<span class="codeph"> -1</span>表示查看集合中的任何图像时始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡出</span> </span> </p> </td> 
   <td colname="col2"> <p>指定文本出现或消失时出现的淡入淡出动画的持续时间。 值<span class="codeph"> 0</span>表示没有淡入淡出过渡。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
