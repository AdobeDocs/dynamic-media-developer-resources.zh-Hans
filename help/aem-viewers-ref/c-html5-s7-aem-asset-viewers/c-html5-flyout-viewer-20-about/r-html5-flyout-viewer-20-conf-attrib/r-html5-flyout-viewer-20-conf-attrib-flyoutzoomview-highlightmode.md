---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高亮|光标 </span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的导航框架的类型。 当设置为 <span class="codeph"> 光标 </span>时，组件使用固定大小的参考光标。 桌面系统和触控设备可能有不同的光标图，它由 <span class="codeph"> .s7cursor </span> CSS类和 <span class="codeph"> input=mouse|touch属性选择器控 </span> 制。 在桌面系统上，锚点位于光标区域的中间，而在触控设备上，锚点位于光标的下中心。 当设置为高 <span class="codeph"> 亮显 </span>示时，组件使用可变大小的导航框架；框架的大小和形状取决于缩放因子和弹出视图的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 观看时 </span> 间 </span> </p> </td> 
   <td colname="col2"> <p> 设置用户激活突出显示或光标后淡入所需的时间（以秒为单位）。 淡入仅适用于触控设备；在桌面系统上，组件将忽略它。 </p> <p>淡入适用于以下UI元素：高光框、固定光标、叠加(在叠 <span class="codeph"> 加参 </span> 数设置为1时 <span class="codeph"> ) </span>。 弹出视图动画仅在高光／光标淡入动画完成后开始。 没有淡出动画。 当用户停用弹出窗口时，相应的UI元素（光标、高亮和叠加）会立即隐藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> 控制导航框架的定位。 </p> <p>如果设置为 <span class="codeph"> 在图 </span> 像上，则导航框架只能位于主视图中实际图像区域内。 </p> <p>如果设置为 <span class="codeph"> “自 </span> 由”，则用户可以将导航框架移动到逻辑主视图区域中的任意位置，甚至可移动到图像内容之外。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
