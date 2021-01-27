---
description: 配置组件在调整大小期间如何为主视图获取新图像和弹出图像。
seo-description: 配置组件在调整大小期间如何为主视图获取新图像和弹出图像。
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic Media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

配置组件在调整大小期间如何为主视图获取新图像和弹出图像。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`宽`*[; *`度`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>当设置为<span class="codeph"> 0 </span>时，组件在调整大小时不会加载新图像，并且弹出视图中的图像分辨率不会更改。 </p> <p>如果设置为<span class="codeph"> 1 </span>，则允许您为加载到主视图中的图像指定一个或多个宽度断点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 断点， <span class="varname"> 宽 </span>度[; <span class="varname"> 宽度 </span>]  </span> </p> </td> 
   <td colname="col2"> <p>加载到主视图的图像的宽度断点。 组件将始终使用最适合初始加载的大小。 调整大小后，它将确保在主视图下始终下载图像，其宽度等于最接近的较大断点，并在客户端上缩小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
