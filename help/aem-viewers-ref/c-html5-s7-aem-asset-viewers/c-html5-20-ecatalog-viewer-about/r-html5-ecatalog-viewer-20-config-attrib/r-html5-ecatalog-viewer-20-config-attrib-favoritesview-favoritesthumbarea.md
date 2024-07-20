---
title: FavoritesView.favoritesThumbView
description: FavoritesView.favoritesThumbView
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 5c57fcc8-be67-408a-9c4c-4e15d5fe6410
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 4%

---

# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`区域`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">区域</span></span> </p> </td> 
   <td colname="col2"> <p> 指定收藏夹缩略图的裁切区域。 表示为总帧大小的相对值，范围从<span class="codeph"> 0</span>到<span class="codeph"> 1.0</span>。 </p> <p>值为<span class="codeph"> 1</span>表示整个帧图像用于缩略图。 </p> <p>值为<span class="codeph"> 0.1</span>表示仅使用帧大小的10%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
