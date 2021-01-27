---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic Media
uuid: e72ae5d6-574e-4f30-827c-021ce5dafcee
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 7%

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

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

[!DNL `1`]

## 示例 {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
