---
description: 新增雜訊。 將隨機雜訊新增至前景影像資料或效果圖層的前景。
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---

# op_noise{#op-noise}

新增雜訊。 將隨機雜訊新增至前景影像資料或效果圖層的前景。

`op_noise= *`val`*[,uniform|gaussian[, *`單色`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>雜訊量，以百分比表示（0到100位元整數）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 色彩一致</span> </p> </td> 
   <td colname="col2"> <p>選取均勻雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 高斯</span> </p> </td> 
   <td colname="col2"> <p>選取高斯雜訊分佈。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 單色</span> </p> </td> 
   <td colname="col2"> <p>設定為0代表色彩雜訊，設為1代表灰色雜訊。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* 會略過灰階影像。

## 屬性 {#section-1f1a64c791f545a3bf1abd0b0e575d87}

圖層指令。 套用至目前圖層或複合影像，如果 `layer=comp`.

## 默认 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`，表示沒有雜訊。
