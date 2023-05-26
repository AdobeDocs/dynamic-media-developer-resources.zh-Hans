---
title: FlyoutZoomView.imagereload
description: 配置组件如何在调整大小期间为主视图和弹出视图获取新图像。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

配置组件如何在调整大小期间为主视图和弹出视图获取新图像。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`宽度`*[; *`宽度`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>当设置为 <span class="codeph"> 0 </span>，组件在调整大小期间不会加载新图像，并且弹出视图中的图像分辨率不会更改。 </p> <p>当设置为 <span class="codeph"> 1 </span> 用于为加载到主视图中的图像指定一个或多个宽度断点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 断点， <span class="varname"> 宽度 </span>[； <span class="varname"> 宽度 </span>] </span> </p> </td> 
   <td colname="col2"> <p>加载到主视图中的图像的宽度断点。 组件始终对初始负载使用最佳适应大小。 在调整大小后，它可确保主视图中的图像下载时宽度始终等于最近的较大断点，并在客户端上缩小尺寸。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
