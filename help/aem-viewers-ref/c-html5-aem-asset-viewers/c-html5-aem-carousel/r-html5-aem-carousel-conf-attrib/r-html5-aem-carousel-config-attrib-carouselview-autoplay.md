---
description: 传送查看器的配置属性。
seo-description: 传送查看器的配置属性。
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.autoplay{#carouselview-autoplay}

传送查看器的配置属性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][，持续时间][，方向]</span> </p> </td> 
   <td colname="col2"> <p> 指定开／关、持续时间，以在传送中显示每个横幅以及自动循环的方向。 </p> <p>设置为 <span class="codeph"> 0</span> ，自动循环关闭。 </p> <p>将 <span class="codeph"> 1设置为</span> “自动开启”,过渡持续时间以秒为单位由持续时间 <span class="codeph"> 控制</span>。 </p> <p>自动回路方向由方向控制 <span class="codeph"></span>。 方 <span class="codeph"> 向</span> ，从右至左至右的范围为1 <span class="codeph"> ,</span> 从左至右的范围为0 <span class="codeph"></span> 。 </p> </td> 
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

