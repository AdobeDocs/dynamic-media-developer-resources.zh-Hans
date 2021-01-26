---
description: 添加杂色。 将随机噪声添加到前景图像数据或效果图层的前景中。
seo-description: 添加杂色。 将随机噪声添加到前景图像数据或效果图层的前景中。
seo-title: op_noise
solution: Experience Manager
title: op_noise
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---


# op_noise{#op-noise}

添加杂色。 将随机噪声添加到前景图像数据或效果图层的前景中。

`op_noise= *``*[,uniform|gaussian[, *`Valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>噪声量（百分比）(0...100 int)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 均匀</span> </p> </td> 
   <td colname="col2"> <p>选择均匀的杂色分布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 高斯</span> </p> </td> 
   <td colname="col2"> <p>选择高斯噪声分布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 单色</span> </p> </td> 
   <td colname="col2"> <p>对于颜色杂色，设置为0；对于灰度杂色，设置为1。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 将忽略灰度图像。

## 属性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, for noonise.
