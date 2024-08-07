---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`升级`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定弹出视图相对于主视图的图像缩放比率。 必须为大于或等于<span class="codeph"> 1.0</span>的整数或浮点值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> 可指定可选次要因子，当高亮处于活动状态时，单击或点按主视图可访问可选次要因子。 再次单击或点按将还原为主缩放因子。 值为<span class="codeph"> -1</span>将禁用次要缩放因子。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">升级</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件处理小图像的方式。 </p> <p>如果设置为<span class="codeph"> 1</span>，则组件将放大主图像，以使其适合主视图。 此外，它还可以放大缩放图像，以便完全填充配置的弹出窗口区域。 </p> <p>如果设置为<span class="codeph"> 0</span>，则以原始分辨率显示小图像，并在主视图区域和弹出窗口内部居中显示。 您可以配置在主视图和弹出窗口中分别使用<span class="codeph"> s7flyoutzoomview</span>和<span class="codeph"> s7flyoutzoom</span> CSS类的背景或类似CSS属性的图像周围出现的额外空格。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
