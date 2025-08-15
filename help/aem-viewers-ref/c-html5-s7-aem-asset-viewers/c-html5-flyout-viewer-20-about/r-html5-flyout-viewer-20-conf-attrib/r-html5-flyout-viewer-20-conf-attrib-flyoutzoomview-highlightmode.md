---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`显示时间`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高亮|光标</span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的导航框架的类型。 当设置为<span class="codeph">游标</span>时，组件使用固定大小的引用游标。 对于桌面系统和触摸设备，可以有不同的光标艺术。 此功能通过<span class="codeph"> .s7cursor </span> CSS类和<span class="codeph"> input=mouse|touch </span>属性选择器来控制。 在桌面系统上，锚点设置在光标区域的中间，而在触控设备上，锚点设置在光标的底部中心。 当设置为<span class="codeph">高亮</span>时，组件使用可变大小的导航框架；框架的大小和形状取决于缩放因子和弹出视图的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">显示时间</span> </span> </p> </td> 
   <td colname="col2"> <p> 设置用户激活高亮或光标后淡入所需的时间（以秒为单位）。 淡入功能仅适用于触控设备；在桌面系统上，它会被组件忽略。 </p> <p>淡入应用于以下UI元素：高亮框架、固定光标、叠加（如果<span class="codeph">叠加</span>参数设置为<span class="codeph"> 1 </span>）。 弹出视图动画仅在高亮/光标在动画中淡入完成后开始。 没有渐隐动画。 当用户停用弹出项时，相应的UI元素（光标、高亮和叠加）会立即隐藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">图像|可用</span> </p> </td> 
   <td colname="col2"> <p> 控制导航框架位置。 </p> <p>如果图像<span class="codeph">上设置为</span>，则导航框架只能位于主视图中的实际图像区域内。 </p> <p>如果设置为<span class="codeph"> free </span>，则用户可以将导航框架移动到逻辑主视图区域中的任意位置，甚至移动到图像内容之外的位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
