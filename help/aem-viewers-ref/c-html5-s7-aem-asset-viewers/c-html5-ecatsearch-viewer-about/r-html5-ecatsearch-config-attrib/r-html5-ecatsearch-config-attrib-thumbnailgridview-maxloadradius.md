---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,Business Practitioner
exl-id: acbcea10-950d-4f98-be5a-5aead9f4e0d9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预加载行为。 </p> <p>当设置为<span class="codeph"> -1</span>时，缩略图会在组件初始化或资产更改时同时加载。 </p> <p>当设置为<span class="codeph"> 0</span>时，只加载可见的缩略图。 </p> <p>设置<span class="codeph"><span class="varname"> preloadnbr</span></span>可定义预加载可见区域周围的不可见行/列数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-a3abd04c03e14c238a07349ce50d8310}

可选。

## 默认 {#section-c60e81667965460cbf03378a1ab9b187}

[!DNL `1`]

## 示例 {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
