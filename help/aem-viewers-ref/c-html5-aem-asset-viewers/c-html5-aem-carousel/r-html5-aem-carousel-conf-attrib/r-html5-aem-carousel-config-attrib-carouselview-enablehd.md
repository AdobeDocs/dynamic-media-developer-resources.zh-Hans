---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">始终|从不|限制</span> </p> </td> 
   <td colname="col2"> <p> 允许、限制或禁止对<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备进行优化，这些设备是指具有高密度显示的设备，如iPhone4和类似设备。 </p> <p>如果处于活动状态，则组件会限制IS图像请求的大小，就像设备只有<span class="codeph"> 1</span>的像素比一样，这样会减少带宽。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph">限制</span>设置，则组件将启用高像素密度，但最多只能启用指定的限制。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
