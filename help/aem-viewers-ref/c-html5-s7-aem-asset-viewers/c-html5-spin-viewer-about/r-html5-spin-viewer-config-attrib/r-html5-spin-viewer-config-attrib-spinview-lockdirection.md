---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
TQID: 'https://experienceleague.adobe.com/eTB-wD8G7HGSDgohQn-FsCeFL1GHMBiqzNUtT3nw5n4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> 指定如果存在2D旋转集，是否允许更改旋转方向。 </p> <p>当设置为<span class="codeph"> 1 </span>时，组件会在手势开始时识别主拖动或轻扫方向（水平与垂直）。 之后，它会保持该方向直到该手势结束。 例如，如果用户启动水平旋转，然后决定继续其在垂直方向上的拖动手势，则组件不会执行垂直旋转。 相反，它只考虑鼠标或轻扫的水平移动。 </p> <p>值为<span class="codeph"> 0 </span>允许用户在手势进行过程中随时更改旋转方向。 如果旋转集为1D，则该设置不起作用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
