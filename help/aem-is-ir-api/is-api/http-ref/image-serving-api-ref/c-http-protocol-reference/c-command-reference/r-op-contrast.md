---
description: 调整对比度。 通过增加亮度超过50%的像素的亮度和亮度低于50%的像素的亮度来调整图像对比度。
seo-description: 调整对比度。 通过增加亮度超过50%的像素的亮度和亮度低于50%的像素的亮度来调整图像对比度。
seo-title: op_contrast
solution: Experience Manager
title: op_contrast
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---


# op_contrast{#op-contrast}

调整对比度。 通过增加亮度超过50%的像素的亮度和亮度低于50%的像素的亮度来调整图像对比度。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>对比度调整百分比(-100..100 int)。 </p></td> 
 </tr> 
</table>

## 属性 {#section-d319ed55057344eab0a3c93f720acdbf}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。

## 默认 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，因为对比度没有变化。在应用操作之前，CMYK图像或图层将转换为RGB。

## 示例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低较高质量图像图层的对比度和锐度，使其与低质量背景照片视觉匹配：

… `&op_blur=3&op_contrast=-12&`

将来的版本可能会使用图像的中值亮度，而不是固定的50%亮度。
