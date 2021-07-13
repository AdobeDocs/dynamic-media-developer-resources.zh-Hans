---
description: 配置组件在调整大小期间如何为主视图和弹出视图获取新图像。
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

配置组件在调整大小期间如何为主视图和弹出视图获取新图像。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`widthwidth`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>当设置为<span class="codeph"> 0 </span>时，组件在调整大小期间不会加载新图像，并且弹出视图中的图像分辨率不会更改。 </p> <p>当设置为<span class="codeph"> 1 </span>时，您可以为加载到主视图中的图像指定一个或多个宽度断点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 断点， <span class="varname"> 宽 </span>度[; <span class="varname"> 宽 </span>度]  </span> </p> </td> 
   <td colname="col2"> <p>加载到主视图中的图像的宽度断点。 组件将始终使用最佳大小进行初始加载。 调整大小后，将确保在主视图中下载的图像的宽度始终等于最接近的较大断点，并在客户端上缩小该断点的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
