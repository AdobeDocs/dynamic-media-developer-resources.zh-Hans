---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
uuid: ad423dc7-4dd8-42d9-bf75-db8f309f6aaa
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持续`*[, *``*][, *`反淡`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间</span> </span> </p> </td> 
   <td colname="col2"> <p>指定提示文本隐藏前显示的秒数。 设置为<span class="codeph"> -1</span>时，即使用户激活弹出，消息也始终显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span> </span> </p> </td> 
   <td colname="col2"> <p>指定查看集合中的新图像时显示文本的次数。 值<span class="codeph"> -1</span>表示查看集合中的任何图像时始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡入</span> </span> </p> </td> 
   <td colname="col2"> <p>指定文本出现或消失时出现的淡入淡出动画的持续时间。 值<span class="codeph"> 0</span>表示没有淡入过渡。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
