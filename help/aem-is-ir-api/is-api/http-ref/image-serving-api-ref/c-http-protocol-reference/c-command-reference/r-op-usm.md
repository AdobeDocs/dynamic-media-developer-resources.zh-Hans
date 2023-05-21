---
description: 不銳利化遮色片。 如果圖層=comp，則在所有縮放之後，對圖層或最終檢視影像進行遮色片銳利化調整。
solution: Experience Manager
title: op_usm
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 6%

---

# op_usm{#op-usm}

不銳利化遮色片。 如果圖層=comp，則在所有縮放之後，對圖層或最終檢視影像進行遮色片銳利化調整。

這些引數會假設為套用至完整解析度的影像，並在處理縮減取樣影像時縮小。

`op_usm= *`金額`*[, *`半徑`*[, *`臨界值`*[, *`單色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 数量</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡強度係數（實數0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半徑</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡核心半徑，以畫素為單位（實數0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 阀值</span></span> </p></td> 
  <td class="stentry"> <p>濾鏡臨界值層級（整數0...255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 單色</span></span> </p></td> 
  <td class="stentry"> <p>設為0可分別套用至每個色彩元件，或設為1僅套用至影像亮度（強度）。 </p> <p> <span class="codeph"><span class="varname"> 單色</span></span> 會略過灰階影像。 </p></td> 
 </tr> 
</table>

圖層遮色片或複合遮色片也會銳利化。

## 屬性 {#section-fb5311b34d164946b74dadb32359518a}

圖層屬性或檢視屬性。 套用至目前圖層或最終檢視影像，如果 `layer=comp`. 被效果圖層忽略。

## 默认 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` 不會產生不銳利化遮色片效果。

## 另请参阅 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ， [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
