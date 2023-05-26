---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: acbcea10-950d-4f98-be5a-5aead9f4e0d9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 5%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预载行为。 </p> <p>当设置为 <span class="codeph"> -1</span> 在初始化组件或更改资产时，将同时加载缩略图。 </p> <p>当设置为 <span class="codeph"> 0</span> 仅加载可见的缩略图。 </p> <p>设置 <span class="codeph"><span class="varname"> preloadnbr</span></span> 定义可见区域周围预载多少不可见的行/列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-a3abd04c03e14c238a07349ce50d8310}

可选.

## 默认 {#section-c60e81667965460cbf03378a1ab9b187}

[!DNL `1`]

## 示例 {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
