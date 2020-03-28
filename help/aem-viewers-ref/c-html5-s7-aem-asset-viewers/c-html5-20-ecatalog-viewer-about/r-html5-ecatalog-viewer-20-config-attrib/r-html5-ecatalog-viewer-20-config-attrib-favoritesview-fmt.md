---
description: 'null'
seo-description: 'null'
seo-title: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
topic: Dynamic media
uuid: 4d9d161e-e39b-4607-9fb1-9dbfb06d7704
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件用于从图像服务器加载图像的图像格式。 格式是图像服务器和客户端浏览器支持的任何值。 </p> <p>如果图像格式以 <span class="codeph"> -alpha结尾</span>，则组件会将图像渲染为透明内容。 对于所有其他图像格式值，组件将图像视为不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
