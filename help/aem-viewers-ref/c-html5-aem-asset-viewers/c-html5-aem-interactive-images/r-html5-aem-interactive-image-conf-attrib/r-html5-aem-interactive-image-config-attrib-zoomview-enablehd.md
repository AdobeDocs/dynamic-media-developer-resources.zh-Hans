---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: b3cc32ef-dd6c-47a3-9e55-86a43e874a84
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 3%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">始终|从不|限制</span> </p> </td> 
   <td colname="col2"> <p> 允许、限制或禁止对<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备进行优化。 会影响具有高密度显示的设备，如iPhone4和类似设备。 如果处于活动状态，则组件会限制IS图像请求的大小，就像设备的像素比为<span class="codeph"> 1</span>一样，从而会减少带宽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制设置，则组件仅在指定限制内启用高像素密度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
