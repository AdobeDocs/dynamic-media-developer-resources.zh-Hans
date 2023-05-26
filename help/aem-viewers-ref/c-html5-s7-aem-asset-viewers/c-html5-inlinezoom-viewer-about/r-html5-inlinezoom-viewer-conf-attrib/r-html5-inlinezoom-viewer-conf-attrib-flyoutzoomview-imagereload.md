---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`宽度`*[; *`宽度`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 配置组件如何在调整大小期间为主视图和弹出视图获取新图像。 </p> <p>设置为 <span class="codeph"> 0 </span>，组件在调整大小期间不会加载新图像，并且弹出视图中的图像分辨率不会更改。 </p> <p>设置为 <span class="codeph"> 1 </span> 用于为加载到主视图中的图像指定一个或多个宽度断点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 断点， <span class="varname"> 宽度 </span>； <span class="varname"> 宽度 </span> </span> </p> </td> 
   <td colname="col2"> <p>加载到主视图中的图像的宽度断点。 </p> <p>组件始终使用初始载荷的最佳配合尺寸。 在调整大小后，它可确保主视图中的图像始终使用与最接近的较大断点相同的宽度下载，并在客户端上缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
