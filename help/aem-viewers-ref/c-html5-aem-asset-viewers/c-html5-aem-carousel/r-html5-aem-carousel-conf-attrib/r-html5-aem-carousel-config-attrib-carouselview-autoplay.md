---
description: 传送查看器的配置属性。
seo-description: 传送查看器的配置属性。
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic Media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---


# CarouselView.autoplay{#carouselview-autoplay}

传送查看器的配置属性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][，持续时间][，方向]</span> </p> </td> 
   <td colname="col2"> <p> 指定开启／关闭、持续时间以在传送和自动循环方向中显示每个横幅。 </p> <p>设置为<span class="codeph"> 0</span>以关闭自动循环。 </p> <p>将<span class="codeph"> 1</span>设置为自动循环，过渡持续时间（以秒为单位）由<span class="codeph">持续时间</span>控制。 </p> <p>自动回路的方向以<span class="codeph">方向</span>进行控制。 <span class="codeph">方向</span>的范围为从右至左和从左至右的<span class="codeph">1</span>和<span class="codeph">0</span>。 </p> </td> 
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

