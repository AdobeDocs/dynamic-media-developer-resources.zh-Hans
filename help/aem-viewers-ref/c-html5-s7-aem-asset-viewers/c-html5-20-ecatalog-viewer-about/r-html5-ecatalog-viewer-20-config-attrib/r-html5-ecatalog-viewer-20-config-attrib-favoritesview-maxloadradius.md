---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
topic: Dynamic media
uuid: 52347bee-2cdf-4bb4-bb6f-eefff06b82af
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 7%

---


# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定组件预载行为。 </p> <p>如果设置为<span class="codeph"> -1</span>，则在初始化组件或更改资产时，会同时加载所有缩略图。 </p> <p>设置为<span class="codeph"> 0</span>时，只加载可见的缩略图。 </p> <p> 当设置为<span class="codeph"><span class="varname"> preloadnbr</span></span>时，可指定预加载可见区域周围的不可见行数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
