---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`宽度`*[; *`宽度`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 配置组件如何在调整大小期间为主视图和弹出视图获取新图像。 </p> <p>当设置为<span class="codeph"> 0 </span>时，组件在调整大小期间不会加载新图像；弹出视图中的图像分辨率不会更改。 </p> <p>设置为<span class="codeph"> 1 </span>允许您为加载到主视图的图像指定一个或多个宽度断点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">断点，<span class="varname">宽度</span>[； <span class="varname">宽度</span>] </span> </p> </td> 
   <td colname="col2"> <p> 加载到主视图的图像的宽度断点。 组件始终使用初始载荷的最佳配合尺寸。 在调整大小后，它可确保主视图中的图像始终以与最近的较大断点相同的宽度下载，并在客户端上按比例缩小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
