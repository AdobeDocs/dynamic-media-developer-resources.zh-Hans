---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic Media
uuid: 7c63a7c5-ac75-485d-94ac-d1e133fbe44f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivitySensitivity `*[, *`Sensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制通过鼠标拖动或轻扫执行的水平和垂直旋转的灵敏度。 </p> <p> <span class="codeph"> </span> xSensitivity设置如果用户水平拖动鼠标从视图的一侧拖动到另一侧，将进行多少次水平产品旋转。例如，“三”表示用户看到一个完全拖动手势的三个完整旋转。 </p> <p>同样，<span class="codeph"> ySensitivity</span>控制垂直旋转的灵敏度。 如果值为1，则表示一次垂直完全拖动或轻扫将视图角从最顶部的旋转平面更改为最底部（反之亦然）。 </p> <p>为<span class="codeph"> ySensitivity</span>设置负值将反转垂直旋转的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
