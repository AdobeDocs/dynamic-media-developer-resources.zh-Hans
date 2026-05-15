---
title: 旋转视图。敏感度
description: 旋转视图。敏感度
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
TQID: 'https://experienceleague.adobe.com/xRqLAbFehJYLGgevPmISxILSWWyedyBSDkbNZTDs808'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# 旋转视图。敏感度{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`x敏感度`*[, *`y敏感度`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[， <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制通过鼠标拖动或轻扫执行的水平和垂直旋转灵敏度。 </p> <p> <span class="codeph"> xSensitivity</span>设置用户将鼠标从视图的一侧水平拖动到另一侧时产品完全水平旋转的次数。 例如，三个表示用户看到一个全拖动手势的三个完整旋转。 </p> <p>同样，<span class="codeph"> ySensitivity</span>控制垂直旋转的敏感度。 值为1表示一次完全垂直拖动或轻扫会将视角从最上旋转平面更改为最下旋转平面（或相反）。 </p> <p>为<span class="codeph"> ySensitivity</span>设置负值将反转垂直旋转方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
