---
description: 'null'
seo-description: 'null'
seo-title: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 7c63a7c5-ac75-485d-94ac-d1e133fbe44f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制通过鼠标拖动或轻扫执行的水平和垂直旋转的敏感度。 </p> <p> <span class="codeph"> xSensitivity</span> 设置当用户将鼠标从视图的一侧水平拖动到另一侧时进行的完全水平产品旋转数。 例如，“三”表示用户看到一个完全拖动手势的三个完整旋转。 </p> <p>同样， <span class="codeph"> ySensitivity</span> （灵敏度）控制垂直旋转的灵敏度。 值1表示一次完全垂直拖动或轻扫将视图角从最顶部的旋转平面更改为最底部的旋转平面（反之亦然）。 </p> <p>为 <span class="codeph"> ySensitivity设置负值</span> ，将反转垂直旋转的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
