---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 5badee0b-3bbc-4306-bc60-a606775db2bd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 对devicePixelRatio大于1的设备启用、限 <span class="codeph"> 制或禁用优</span> 化 <span class="codeph"></span>。 影响具有高密度显示屏（如iPhone4和类似设备）的设备。 如果处于活动状态，则该组件将限制IS图像请求的大小，就像设备具有1的像素比一样 <span class="codeph"></span>，从而减少带宽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制设置，则组件仅启用高像素密度，而不超过指定的限制。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
