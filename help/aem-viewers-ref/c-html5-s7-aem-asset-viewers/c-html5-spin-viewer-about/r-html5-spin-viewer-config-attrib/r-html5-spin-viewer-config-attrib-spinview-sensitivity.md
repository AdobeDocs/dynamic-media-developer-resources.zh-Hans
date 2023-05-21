---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`敏感度`*[, *`敏感度`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 敏感度</span>[， <span class="varname"> 敏感度</span>]</span> </p> </td> 
   <td colname="col2"> <p> 控制使用滑鼠拖曳或撥動執行的水平與垂直迴轉的敏感度。 </p> <p> <span class="codeph"> 敏感度</span> 設定當使用者從檢視的一側水準拖曳滑鼠到另一側時，產品會進行幾次完全水準旋轉。 例如，三個表示使用者看到一個完整拖曳手勢的三個完整旋轉。 </p> <p>同樣地， <span class="codeph"> 敏感度</span> 控制垂直迴轉的敏感度。 值1表示一次垂直拖曳或撥動會將檢視角度從最上方的旋轉平面變更為最下方（反之亦然）。 </p> <p>設定負值 <span class="codeph"> 敏感度</span> 反轉垂直迴轉的方向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
