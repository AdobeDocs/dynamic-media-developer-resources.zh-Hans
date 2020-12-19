---
description: 'null'
seo-description: 'null'
seo-title: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic media
uuid: 13ea3917-346a-47c3-a535-f771910fa1c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 10%

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预载行为。 </p> <p>如果设置为<span class="codeph"> -1</span>，则在初始化组件或资产更改时，会同时加载缩略图。 </p> <p>设置为<span class="codeph"> 0</span>时，仅加载可见的缩略图。 </p> <p>设置<span class="codeph"><span class="varname"> preloadnbr</span></span>定义预加载可见区域周围的不可见行／列数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-a3abd04c03e14c238a07349ce50d8310}

可选。

## 默认 {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## 示例 {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
