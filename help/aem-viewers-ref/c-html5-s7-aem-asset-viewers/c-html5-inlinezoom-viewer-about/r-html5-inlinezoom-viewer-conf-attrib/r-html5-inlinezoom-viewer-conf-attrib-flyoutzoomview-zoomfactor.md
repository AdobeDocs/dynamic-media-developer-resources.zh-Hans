---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic Media
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`PrimaryFactorsecondaryFactors放`*[,[ *``*][, *`大`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定弹出视图相对于主视图的图像放大率。必须为整数或浮点值<span class="codeph"> 1.0</span>或更大。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 可以指定可选的辅助因子，当高亮处于活动状态时，单击或点按主视图即可访问该辅助因子。 再次单击或点按时间会还原为主缩放因子。 值<span class="codeph"> -1</span>将禁用次缩放因子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高档</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件处理小图像的方式。 </p> <p>如果设置为<span class="codeph"> 1</span>，则组件会上升显示主图像，使其适合主视图。 此外，它还会放大缩放图像，使其完全填充配置的弹出窗口区域。 </p> <p>如果设置为<span class="codeph"> 0</span>，则以其原始分辨率显示小图像，并以主视图区和弹出窗口的中心显示。 您可以在主视图和弹出窗口中分别使用<span class="codeph"> s7flyoutzoomview</span>和<span class="codeph"> s7flyoutzoom</span> CSS类的背景或类似CSS属性配置图像周围的额外空白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
