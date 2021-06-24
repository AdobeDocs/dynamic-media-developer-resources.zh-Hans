---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: Developer,Business Practitioner
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定在2D旋转集的情况下是否允许旋转方向发生更改。 </p> <p>当设置为<span class="codeph"> 1 </span>时，该组件会在手势开始时标识主要的拖动或轻扫方向（水平或垂直）。 之后，它会保持该方向直到手势结束。 例如，如果用户开始水平旋转，然后决定在垂直方向上继续拖动手势，则组件不会执行垂直旋转；相反，它只考虑鼠标的水平移动或轻扫。 </p> <p><span class="codeph"> 0 </span>值允许用户在手势过程中随时更改旋转方向。 如果旋转集为1D，则设置不会受到影响。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
