---
description: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高亮|光标  </span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的导航框架的类型。 当设置为<span class="codeph">游标</span>时，组件使用固定大小的参考游标。 桌面系统和触控设备可能有不同的光标图，这可以通过<span class="codeph"> .s7cursor </span> CSS类和<span class="codeph"> input=mouse|touch </span>属性选择器来控制。 在桌面系统上，锚点设置在光标区域的中间，而在触控设备上，锚点位于光标的下中心。 当设置为<span class="codeph">高亮</span>时，组件使用可变大小的导航框架；框架的大小和形状取决于缩放因子和弹出视图的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 设置用户激活突出显示或光标后淡入所需的时间（以秒为单位）。 淡入仅适用于触控设备；在桌面系统上，组件会忽略它。 </p> <p>淡入适用于以下UI元素：高亮帧、固定光标、叠加（如果<span class="codeph"> overlay </span>参数设置为<span class="codeph"> 1 </span>）。 弹出视图动画仅在动画完成高光/光标淡入之后开始。 没有淡出动画。 当用户停用弹出时，相应的UI元素（光标、高亮和叠加）会立即隐藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> 控制导航框架定位。 </p> <p>如果设置为图像</span>上的<span class="codeph">，则导航框架只能位于主视图中实际图像区域内。 </span></p> <p>如果设置为<span class="codeph">自由</span>，则用户可以将导航框架移动到逻辑主视图区域的任意位置，即使是在图像内容之外。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
