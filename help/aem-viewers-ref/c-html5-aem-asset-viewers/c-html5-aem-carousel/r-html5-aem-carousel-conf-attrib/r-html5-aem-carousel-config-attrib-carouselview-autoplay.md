---
title: CarouselView.autoplay
description: 轮播查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# CarouselView.autoplay{#carouselview-autoplay}

轮播查看器的配置属性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][，duration][，direction]</span> </p> </td> 
   <td colname="col2"> <p> 指定自动循环的打开/关闭、在轮播中显示每个横幅的持续时间以及方向。 </p> <p>设置为<span class="codeph"> 0</span>关闭自动循环。 </p> <p>将<span class="codeph"> 1</span>设置为自动循环，并由<span class="codeph"> duration</span>控制过渡持续时间（以秒为单位）。 </p> <p>自动循环的方向由<span class="codeph">方向</span>控制。 <span class="codeph">方向</span>的范围介于<span class="codeph"> 1</span>从右至左和<span class="codeph"> 0</span>从左至右之间。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
