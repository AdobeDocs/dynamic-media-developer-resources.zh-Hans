---
description: 調整對比。 調整影像對比，增加亮度超過50%的畫素亮度，以及減少亮度低於50%的畫素亮度。
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# op_contrast{#op-contrast}

調整對比。 調整影像對比，增加亮度超過50%的畫素亮度，以及減少亮度低於50%的畫素亮度。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>百分比對比調整（–100...100位元整數）。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-d319ed55057344eab0a3c93f720acdbf}

圖層指令。 套用至目前圖層或複合影像，如果 `layer=comp`. 被效果圖層忽略。

## 默认 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`，對比無變化。 CMYK影像或圖層會在套用作業之前轉換為RGB。

## 示例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

降低較高品質影像層的對比度和銳利度，以視覺上比對低品質的背景像片：

… `&op_blur=3&op_contrast=-12&`

未來版本可能會使用影像的亮度中值，而非固定的50%亮度。
