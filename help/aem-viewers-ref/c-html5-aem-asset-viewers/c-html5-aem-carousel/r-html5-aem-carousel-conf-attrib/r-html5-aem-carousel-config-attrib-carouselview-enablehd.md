---
description: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
topic: Dynamic Media
uuid: 17df4a68-a251-427c-a3c4-1e0679e3f8f1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---


# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始终|从不|限制</span> </p> </td> 
   <td colname="col2"> <p> 对于<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备，即具有高密度显示屏（如iPhone4和类似设备）的设备，启用、限制或禁用优化。 </p> <p>如果处于活动状态，则组件会限制IS图像请求的大小，就像设备仅具有<span class="codeph"> 1</span>的像素比一样，这样可以减少带宽。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph"> limit</span>设置，则组件启用的高像素密度仅达到指定的限制。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
