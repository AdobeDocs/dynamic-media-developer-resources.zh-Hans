---
description: ThumbnailGridView.fmt
solution: Experience Manager
title: ThumbnailGridView.fmt
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog
role: Developer,Business Practitioner
exl-id: 916ee5d1-e398-4923-9107-96f649033298
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

`[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>指定组件用于从图像服务器加载图像的图像格式。 它可以是图像服务器和客户端浏览器支持的任何值。 如果指定的格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件会将图像视为不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

可选。

## 默认 {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## 示例 {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`
