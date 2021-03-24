---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`宽`*[; *`度`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 配置组件在调整大小期间为主图像和弹出视图获取新图像的方式。 </p> <p>当设置为<span class="codeph"> 0 </span>时，组件在调整大小时不会加载新图像；弹出视图中的图像分辨率不会更改。 </p> <p>设置为<span class="codeph"> 1 </span>允许您为加载到主视图的图像指定一个或多个宽度断点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 断点， <span class="varname"> 宽度 </span>[; <span class="varname"> 宽度 </span>]  </span> </p> </td> 
   <td colname="col2"> <p> 加载到主视图的图像的宽度断点。 组件始终对初始加载使用最佳调整大小。 调整大小后，它将确保始终以与最接近的较大断点相等的宽度下载主视图中的图像，并在客户端上缩小该图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
