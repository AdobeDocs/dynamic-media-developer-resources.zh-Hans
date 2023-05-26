---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定如果存在2D旋转集，是否允许旋转方向发生变化。 </p> <p>当设置为 <span class="codeph"> 1 </span>，组件会在手势开始时标识主拖动或轻扫方向（水平与垂直）。 之后，它会保持该方向直到该手势结束。 例如，如果用户开始水平旋转，然后决定继续其在垂直方向上的拖动手势，则组件不会执行垂直旋转。 相反，它只考虑鼠标的水平移动或滑动。 </p> <p>值 <span class="codeph"> 0 </span> 允许用户在手势过程中随时更改旋转方向。 如果旋转集为1D，则该设置不起作用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
