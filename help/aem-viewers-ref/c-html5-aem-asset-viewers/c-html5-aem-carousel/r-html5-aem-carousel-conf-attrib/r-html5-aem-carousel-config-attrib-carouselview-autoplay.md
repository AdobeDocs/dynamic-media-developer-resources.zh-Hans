---
title: CarouselView.autoplay
description: 轮播查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
TQID: 'https://experienceleague.adobe.com/LEeJUVIHLhplymrvp9IdNUWcfJz-Tl0kLffkik1GvkY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

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

## 示例： {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
