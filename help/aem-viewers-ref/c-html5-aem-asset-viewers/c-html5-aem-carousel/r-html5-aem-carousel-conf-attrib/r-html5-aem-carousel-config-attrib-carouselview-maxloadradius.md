---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
uuid: 0dcebbce-f449-4f5f-acbc-02960e1dbdba
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定组件预载行为。 </p> <p>设置为<span class="codeph"> -1</span>时，组件将在空闲状态下预载所有传送帧。 </p> <p>设置为<span class="codeph"> 0</span>时，组件仅加载当前可见、上一帧和下一帧的帧。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>定义当当前显示的帧周围有多少个不可见的帧处于空闲状态时被预加载。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
