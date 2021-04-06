---
description: 传送查看器的配置属性。
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

传送查看器的配置属性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][，持续时间][，方向]</span> </p> </td> 
   <td colname="col2"> <p> 指定开/关、显示自动循环传送中每个横幅的持续时间和方向。 </p> <p>设置为<span class="codeph"> 0</span>以关闭自动循环。 </p> <p>将<span class="codeph"> 1</span>设置为自动循环，过渡持续时间以秒为单位，由<span class="codeph">持续时间</span>控制。 </p> <p>自动回路的方向以<span class="codeph">方向</span>控制。 <span class="codeph">方向</span>具有从右到左和从左到右的<span class="codeph"> 0</span>之间的范围。<span class="codeph"></span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
