---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic Media
uuid: 5badee0b-3bbc-4306-bc60-a606775db2bd
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 7%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始终|从不|限制</span> </p> </td> 
   <td colname="col2"> <p> 对<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备启用、限制或禁用优化。 影响具有高密度显示屏（如iPhone4和类似设备）的设备。 如果处于活动状态，则组件会像设备的像素比<span class="codeph"> 1</span>一样限制IS图像请求的大小，从而减少带宽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制设置，则组件仅启用高像素密度（不超过指定限制）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
