---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高亮|光标 </span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的导航框架的类型。 当设置为 <span class="codeph"> 光标 </span>，则组件使用固定大小的引用游标。 可以对台式机系统和触摸设备使用不同的光标艺术。 此功能可通过 <span class="codeph"> .s7cursor </span> CSS类和 <span class="codeph"> input=mouse|touch </span> 属性选择器。 在桌面系统上，光标区域的中间设置一个锚点，而在触摸设备上，锚点位于光标的底部中心。 当设置为 <span class="codeph"> 突出显示 </span>，则组件使用可变大小的导航框架；框架的大小和形状取决于缩放因子和弹出视图的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> 设置用户激活突出显示或光标后其进入淡入的时间（以秒为单位）。 仅对触控设备应用渐隐；在桌面系统上，组件会忽略该事件。 </p> <p>渐隐应用于以下UI元素：高亮帧，固定光标，叠加(在 <span class="codeph"> 叠加 </span> 参数设置为 <span class="codeph"> 1 </span>)。 弹出视图动画仅在动画完成高亮/光标淡出后开始。 没有淡出动画。 当用户停用弹出窗口时，相应的UI元素（光标、高亮显示和叠加）会立即隐藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> 控制导航框定位。 </p> <p>如果设置为 <span class="codeph"> onimage </span>，则导航框架只能位于主视图内的实际图像区域内。 </p> <p>如果设置为 <span class="codeph"> 免费 </span> 用户可以将导航框架移动到逻辑主视图区域中的任意位置，甚至移动到图像内容之外。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
