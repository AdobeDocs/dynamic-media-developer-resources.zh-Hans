---
description: 钝化蒙版。 如果layer=comp，则在进行所有缩放后，USM锐化图层或最终视图图像。
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---

# op_usmR{#op-usmr}

钝化蒙版。 如果layer=comp，则在进行所有缩放后，USM锐化图层或最终视图图像。

无论是否进行了向下采样，参数都会按原样应用。

`op_usmR= *``*[, *``*[, *``*[, *`amountradiusRthresholdmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 数量</span></span> </p></td> 
  <td class="stentry"> <p>滤镜强度因子（实数0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>以像素为单位筛选内核半径（实数0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 阀值</span></span> </p></td> 
  <td class="stentry"> <p>筛选阈值级别（整数0...255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 单色</span></span> </p></td> 
  <td class="stentry"> <p>将设置为0可分别应用于每个颜色分量，或将设置为1可仅应用于图像亮度（强度）。 </p> <p><span class="codeph"> <span class="varname"> </span></span> 对于灰度图像，将忽略单色。 </p> </td> 
 </tr> 
</table>

图层蒙版或复合蒙版也会被锐化。

## 属性 {#section-fb5311b34d164946b74dadb32359518a}

层属性或视图属性。 如果`layer=comp`，则应用于当前层或最终视图图像。 效果层会忽略它。

## 默认 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` 无USM锐化效果。

## 另请参阅 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
