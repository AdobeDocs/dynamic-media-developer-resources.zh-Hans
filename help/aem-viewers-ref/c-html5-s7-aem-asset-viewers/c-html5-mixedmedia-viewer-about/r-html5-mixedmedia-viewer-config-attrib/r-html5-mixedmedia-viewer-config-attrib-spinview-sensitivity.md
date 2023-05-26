---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`x敏感度`*[, *`y敏感性`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> x敏感度</span>[， <span class="varname"> y敏感性</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制通过鼠标拖动或轻扫执行的水平和垂直旋转灵敏度。 </p> <p> <span class="codeph"> x敏感度</span> 设置当用户将鼠标从视图的一侧水平拖动到另一侧时，产品进行完全水平旋转的次数。 例如，三个表示用户看到一个完全拖动手势的三个完全旋转。 </p> <p>同样， <span class="codeph"> y敏感性</span> 控制垂直旋转的敏感性。 值为1表示一次完全垂直拖动或轻扫会将视角从最上方的旋转平面更改为最下方（或相反）。 </p> <p>设置负值 <span class="codeph"> y敏感性</span> 反转垂直旋转的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
