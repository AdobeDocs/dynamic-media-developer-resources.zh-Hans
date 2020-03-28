---
description: 'null'
seo-description: 'null'
seo-title: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
topic: Dynamic media
uuid: f8369636-08e9-4f00-8562-86a2a907b4fa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`Steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步骤</span></span> </p> </td> 
   <td colname="col2"> <p> 配置将分辨率提高或降低两倍所需的数字放大和缩小操作。 每个缩放操作的分辨率更改是每步2^1。 设置为 <span class="codeph"> 0</span> ，通过一次缩放操作可缩放到全分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相对于全分辨率图像的最大缩放分辨率。 默认值为 <span class="codeph"> 1.0</span>，这不允许缩放超出完整分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选。

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
