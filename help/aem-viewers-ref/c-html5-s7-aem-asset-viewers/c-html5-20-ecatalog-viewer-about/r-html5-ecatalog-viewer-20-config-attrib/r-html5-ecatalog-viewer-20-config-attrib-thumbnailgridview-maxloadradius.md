---
title: ThumbnailGridView.maxloadradius
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 7%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预加载行为。 </p> <p>当设置为 <span class="codeph"> -1</span> 初始化组件或资产更改时，会同时加载缩略图。 </p> <p>当设置为 <span class="codeph"> 0</span> 只加载可见的缩略图。 </p> <p>已设置 <span class="codeph"><span class="varname"> preloadnbr</span></span> 定义预加载可见区域周围的多少行/列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-a3abd04c03e14c238a07349ce50d8310}

可选。

## 默认 {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## 示例 {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
