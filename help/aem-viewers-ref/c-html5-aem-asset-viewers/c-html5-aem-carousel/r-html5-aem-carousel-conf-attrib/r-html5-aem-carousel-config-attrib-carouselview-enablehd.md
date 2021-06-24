---
description: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,Business Practitioner
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 总是|从|不|限制</span> </p> </td> 
   <td colname="col2"> <p> 对于<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备，即具有高密度显示（如iPhone4和类似设备）的设备，启用或禁用优化。 </p> <p>如果处于活动状态，则组件会限制IS图像请求的大小，如同设备仅具有<span class="codeph"> 1</span>的像素比，并且这样会减少带宽。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph"> limit</span>设置，则该组件仅启用高像素密度，而达到指定的限制。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
