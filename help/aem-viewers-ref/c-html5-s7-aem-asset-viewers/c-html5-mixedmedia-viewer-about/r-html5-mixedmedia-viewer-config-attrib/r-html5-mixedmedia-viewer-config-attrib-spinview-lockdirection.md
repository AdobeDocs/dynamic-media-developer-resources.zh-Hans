---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
uuid: b46a3d78-e381-4351-a4f4-a228386df527
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定是否允许在2D旋转集的情况下更改旋转方向。 </p> <p>当设置为<span class="codeph"> 1 </span>时，该组件在手势开始标识主拖动或轻扫方向（水平或垂直）。 之后，它将保持该方向直到手势结束。 例如，如果用户开始了水平旋转，然后决定在垂直方向上继续拖动手势，则组件不会执行垂直旋转；相反，它只考虑鼠标或轻扫的水平移动。 </p> <p>值<span class="codeph"> 0 </span>允许用户在手势过程中随时更改旋转方向。 如果旋转集为1D，则设置不会影响。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
