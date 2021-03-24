---
description: FavoritesView.fmt
solution: Experience Manager
title: FavoritesView.fmt
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 4%

---


# FavoritesView.fmt{#favoritesview-fmt}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件用于从图像服务器加载图像的图像格式。 格式是图像服务器和客户端浏览器支持的任何值。 </p> <p>如果图像格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 对于所有其他图像格式值，组件将图像视为不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
