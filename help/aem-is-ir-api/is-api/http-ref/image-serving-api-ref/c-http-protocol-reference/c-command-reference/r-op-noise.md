---
description: 添加噪音。 向前景图像数据或效果层的前景添加随机噪声。
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# op_noise{#op-noise}

添加噪音。 向前景图像数据或效果层的前景添加随机噪声。

`op_noise= *``*[,uniform|gaussian[, *`valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>噪音量（百分比）(0...100int)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 均匀</span> </p> </td> 
   <td colname="col2"> <p>选择均匀的噪声分布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 高斯</span> </p> </td> 
   <td colname="col2"> <p>选择高斯噪声分布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 单色</span> </p> </td> 
   <td colname="col2"> <p>对于颜色噪声，设置为0；对于灰色噪声，设置为1。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 将忽略灰度图像。

## 属性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

层命令。 应用于当前层或复合图像（如果`layer=comp`）。

## 默认 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`，无噪音。
