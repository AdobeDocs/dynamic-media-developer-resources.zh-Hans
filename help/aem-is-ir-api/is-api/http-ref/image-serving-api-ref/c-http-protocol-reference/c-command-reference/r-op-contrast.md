---
description: 调整对比度。 通过增加亮度超过50%的像素的亮度，以及降低亮度小于50%的像素的亮度来调整图像对比度。
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# op_contrast{#op-contrast}

调整对比度。 通过增加亮度超过50%的像素的亮度，以及降低亮度小于50%的像素的亮度来调整图像对比度。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>对比度调整百分比(-100...100 int)。 </p></td> 
 </tr> 
</table>

## 属性 {#section-d319ed55057344eab0a3c93f720acdbf}

层命令。 应用于当前层或复合图像（如果`layer=comp`）。 被效果层忽略。

## 默认 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，以保持对比度不变。在应用操作之前，CMYK图像或图层将转换为RGB。

## 示例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低较高质量图像图层的对比度和锐度，使其与低质量背景照片视觉上相匹配：

… `&op_blur=3&op_contrast=-12&`

将来的版本可能使用图像的中值亮度，而不是固定的50%亮度。
