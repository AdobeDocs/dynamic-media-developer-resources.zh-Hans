---
description: 添加杂色。 将随机噪声添加到前景图像数据或效果图层的前景中。
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# op_noise{#op-noise}

添加杂色。 将随机噪声添加到前景图像数据或效果图层的前景中。

`op_noise= *`Valmonochrome`*[,uniform|gaussian[, *``*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 瓦尔</span> </p> </td> 
   <td colname="col2"> <p>杂色量（百分比）(0...100 int)。 </p> </td> 
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
   <td colname="col2"> <p>对于颜色杂色，设置为0；对于灰色杂色，设置为1。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 将忽略灰度图像。

## 属性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, for noose.
