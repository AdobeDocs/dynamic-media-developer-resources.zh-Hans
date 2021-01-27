---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
topic: Dynamic Media
uuid: 103097e9-7e6d-413c-a6a8-b8a15665348c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

---


# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`斯`*[, *`特普利特`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步骤</span></span> </p> </td> 
   <td colname="col2"> <p> 配置放大和缩小操作的数量，这些操作要求将分辨率提高或降低两倍。 每个缩放操作的分辨率更改是每步2^1。 设置为<span class="codeph"> 0</span>，通过单个缩放操作缩放到完整分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相对于全分辨率图像的最大缩放分辨率。 默认值为<span class="codeph"> 1.0</span>，它不允许缩放超出完整分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
