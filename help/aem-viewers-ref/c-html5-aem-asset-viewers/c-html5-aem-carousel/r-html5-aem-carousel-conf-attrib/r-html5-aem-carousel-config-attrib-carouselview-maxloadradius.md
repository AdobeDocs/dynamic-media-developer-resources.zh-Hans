---
title: CarouselView.maxloadradius
description: CarouselView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定元件預先載入行為。 </p> <p>當設定為 <span class="codeph"> -1</span> 處於閒置狀態時，元件會預先載入所有輪播影格。 </p> <p>當設定為 <span class="codeph"> 0</span> 元件僅載入目前可見的影格、上一個影格和下一個影格。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>定義在閒置狀態中，目前顯示影格周圍預先載入的不可見影格數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
