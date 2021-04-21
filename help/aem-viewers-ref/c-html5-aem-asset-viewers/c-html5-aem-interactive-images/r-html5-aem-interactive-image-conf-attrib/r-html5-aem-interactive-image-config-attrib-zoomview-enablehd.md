---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: b3cc32ef-dd6c-47a3-9e55-86a43e874a84
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 总是|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 对于<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备启用、限制或禁用优化。 影响具有高密度显示屏（如iPhone4和类似设备）的设备。 如果处于活动状态，则该组件将限制IS图像请求的大小，就像该设备的像素比为<span class="codeph"> 1</span>一样，从而减少带宽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制设置，则组件仅启用高像素密度（高于指定的限制）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
