---
title: PanoramicView.fmt
description: 指定组件从图像服务器加载图像时使用的图像格式。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

指定组件从图像服务器加载图像时使用的图像格式。 如果指定的格式以“ — alpha”结尾，则组件会将图像渲染为透明。 对于所有其他图像格式，组件会将图像视为不透明。 请注意，组件在默认情况下具有透明背景。 因此，要使它不透明，请将 `background-color` CSS属性至 `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> 指定组件从图像服务器加载图像时使用的图像格式。 如果指定的格式以“ — alpha”结尾，组件会将图像渲染为透明内容；对于所有其他图像格式，组件会将图像视为不透明。 请注意，组件在默认情况下具有透明背景，因此为了不透明，请将background-color CSS属性设置为所需颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
