---
title: op_contrast
description: 调整对比度。 通过增加亮度大于50%的像素的亮度以及减少亮度小于50%的像素的亮度来调整图像对比度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# op_contrast{#op-contrast}

调整对比度。 通过增加亮度大于50%的像素的亮度以及减少亮度小于50%的像素的亮度来调整图像对比度。

`op_contrast= *`调整`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">调整</span> </p> </td> 
  <td class="stentry"> <p>以百分比表示的对比度调整（–100...100整数）。 </p></td> 
 </tr> 
</table>

## 属性 {#section-d319ed55057344eab0a3c93f720acdbf}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果层忽略。

## 默认 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，对比度无变化。 在应用操作之前，CMYK图像或图层将转换为RGB。

## 示例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低较高品质图像图层的对比度和锐度，以将其与低品质背景照片进行视觉匹配：

... `&op_blur=3&op_contrast=-12&`

未来版本可能使用图像的亮度中值，而不是固定的50%亮度。
