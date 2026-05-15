---
title: 收藏夹视图.maxloadradius
description: 收藏夹视图.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6bbf75f1-96e7-496d-9f5c-6f449f76bfdd
TQID: 'https://experienceleague.adobe.com/e5J8j5Skr3LZIG-kjfoTwb6-Iu1duI2Lhb6CoDqZ-E8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 5%

---

# 收藏夹视图.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定组件预载行为。 </p> <p>如果设置为<span class="codeph"> -1</span>，则在初始化组件或更改资产时，将同时加载所有缩略图。 </p> <p>当设置为<span class="codeph"> 0</span>时，将只加载可见的缩略图。 </p> <p> 当设置为<span class="codeph"><span class="varname"> preloadnbr</span></span>时，您可以指定预加载可见区域周围多少不可见的行。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
