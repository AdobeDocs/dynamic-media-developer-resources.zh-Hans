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
ht-degree: 6%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定组件预加载行为。 </p> <p>当设置为<span class="codeph"> -1</span>时，组件会在空闲状态下预加载所有轮播帧。 </p> <p>当设置为<span class="codeph"> 0</span>时，组件仅加载当前可见的帧、前一帧和下一帧。 </p> <p><span class="codeph"><span class="varname"> </span></span>preloadnbr定义在空闲状态下预加载当前显示框架周围的不可见框架数量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
