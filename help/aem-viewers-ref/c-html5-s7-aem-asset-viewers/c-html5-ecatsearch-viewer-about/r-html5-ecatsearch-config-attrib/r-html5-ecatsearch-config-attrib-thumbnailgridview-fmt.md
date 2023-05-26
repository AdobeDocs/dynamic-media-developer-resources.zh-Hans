---
description: ThumbnailGridView.fmt
solution: Experience Manager
title: ThumbnailGridView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ff57762e-05f5-41c1-956f-39280941eeb1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>指定组件从图像服务器加载图像时使用的图像格式。 它可以是Image Server和客户端浏览器支持的任意值。 如果指定的格式结尾为 <span class="codeph"> -alph</span>，组件会将图像渲染为透明内容。 对于所有其他图像格式，组件会将图像视为不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

可选.

## 默认 {#section-502c098dbae1452180c7f575a1d9dc8b}

[!DNL `jpeg`]

## 示例 {#section-5cde7b856ba646c293cfd3d79e47c507}

[!DNL `fmt-png-alpha`]
