---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: Developer,Business Practitioner
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`widthwidth`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 配置组件在调整大小期间如何为主视图和弹出视图获取新图像。 </p> <p>如果设置为<span class="codeph"> 0 </span>，则组件在调整大小期间不会加载新图像，并且弹出视图中的图像分辨率不会更改。 </p> <p>设置为<span class="codeph"> 1 </span>允许您为加载到主视图中的图像指定一个或多个宽度断点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 断点、宽 <span class="varname"> 度 </span>; <span class="varname"> 宽度  </span> </span> </p> </td> 
   <td colname="col2"> <p>加载到主视图中的图像的宽度断点。 </p> <p>组件始终使用最适合的大小来进行初始加载。 调整大小后，它可确保始终使用宽度等于最接近的较大断点来下载主视图中的图像，并在客户端上缩小该图像的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
