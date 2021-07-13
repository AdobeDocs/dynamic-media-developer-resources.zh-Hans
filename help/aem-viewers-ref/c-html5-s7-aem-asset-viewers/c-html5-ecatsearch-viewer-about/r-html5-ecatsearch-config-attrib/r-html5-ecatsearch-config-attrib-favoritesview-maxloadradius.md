---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,User
exl-id: 440f147e-865c-4615-8d83-ea6431271612
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定组件预加载行为。 </p> <p>如果设置为<span class="codeph"> -1</span>，则在初始化组件或更改资产时，会同时加载所有缩略图。 </p> <p>当设置为<span class="codeph"> 0</span>时，只加载可见的缩略图。 </p> <p> 当设置为<span class="codeph"><span class="varname"> preloadnbr</span></span>时，您可以指定预加载可见区域周围的不可见行数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `1`]

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `maxloadradius=0`]
