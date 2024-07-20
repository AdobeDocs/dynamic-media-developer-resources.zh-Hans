---
title: op噪声
description: 添加噪音。 将随机噪声添加到前景图像数据，或添加到效果图层的前景中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---

# op噪声{#op-noise}

添加噪音。 将随机噪声添加到前景图像数据，或添加到效果图层的前景中。

`op_noise= *`val`*[,uniform|gaussian[, *`单色`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">值</span> </p> </td> 
   <td colname="col2"> <p>噪音量，以百分比表示(0...100 int)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">制服</span> </p> </td> 
   <td colname="col2"> <p>选择均匀噪声分布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">高斯</span> </p> </td> 
   <td colname="col2"> <p>选择高斯噪声分布。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname">单色</span> </p> </td> 
   <td colname="col2"> <p>设置为0表示颜色杂色，设置为1表示灰色杂色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

对于灰度图像忽略&#x200B;*`monochrome`*。

## 属性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`，无噪音。
