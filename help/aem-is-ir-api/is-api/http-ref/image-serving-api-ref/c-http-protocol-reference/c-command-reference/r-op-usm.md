---
description: 钝化蒙版。 如果图层为comp，则在全部缩放后，对图层或最终视图图像进行USM锐化。
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

钝化蒙版。 如果图层为comp，则在全部缩放后，对图层或最终视图图像进行USM锐化。

假设这些参数适用于全分辨率图像，并在处理缩减像素取样图像时按比例缩小。

`op_usm= *`数量`*[, *`半径`*[, *`阈值`*[, *`单色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 数量</span></span> </p></td> 
  <td class="stentry"> <p>滤镜强度因子（实数0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半径</span></span> </p></td> 
  <td class="stentry"> <p>滤镜内核半径，以像素为单位（实数0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 阀值</span></span> </p></td> 
  <td class="stentry"> <p>滤镜阈值级别（整数0...255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 单色</span></span> </p></td> 
  <td class="stentry"> <p>设置为0将分别应用至每个颜色组件，或者设置为1将仅应用至图像亮度（强度）。 </p> <p> <span class="codeph"><span class="varname"> 单色</span></span> 对于灰度图像，将忽略。 </p></td> 
 </tr> 
</table>

该图层掩模或复合掩模也被锐化。

## 属性 {#section-fb5311b34d164946b74dadb32359518a}

层属性或视图属性。 应用于当前图层或最终视图图像，如果 `layer=comp`. 被效果层忽略。

## 默认 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` 不会产生钝化蒙版效果。

## 另请参阅 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ， [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
