---
description: USM锐化。 如果layer=comp，则在进行缩放后，USM锐化图层或最终视图图像。
seo-description: USM锐化。 如果layer=comp，则在进行缩放后，USM锐化图层或最终视图图像。
seo-title: op_usm
solution: Experience Manager
title: op_usm
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c647e063-2405-489b-b14d-a70638ac8af7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 7%

---


# op_usm{#op-usm}

USM锐化。 如果layer=comp，则在进行缩放后，USM锐化图层或最终视图图像。

假定这些参数应用于全分辨率图像并在处理缩减采样图像时缩小。

`op_usm= *`单`*[, *``*[, *``*[, *`色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 数量</span></span> </p></td> 
  <td class="stentry"> <p>滤镜强度因子（实数0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半径</span></span> </p></td> 
  <td class="stentry"> <p>筛选内核半径（以像素为单位）（实数0..250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 阀值</span></span> </p></td> 
  <td class="stentry"> <p>筛选器阈值级别(int 0...255)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 单色</span></span> </p></td> 
  <td class="stentry"> <p>设置为0可分别应用于每个颜色组件，设置为1可仅应用于图像亮度（强度）。 </p> <p> <span class="codeph"><span class="varname"> 灰</span></span> 度图像忽略单色。 </p></td> 
 </tr> 
</table>

图层蒙版或复合蒙版也会被锐化。

## 属性 {#section-fb5311b34d164946b74dadb32359518a}

图层属性或视图属性。 应用于当前层或最终视图图像（如果`layer=comp`）。 被效果图层忽略。

## 默认 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` 无USM锐化效果。

## 另请参阅 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)
