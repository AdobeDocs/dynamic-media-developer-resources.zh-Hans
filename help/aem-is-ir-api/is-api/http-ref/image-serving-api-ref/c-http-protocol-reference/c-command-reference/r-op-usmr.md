---
title: op_usmR
description: 钝化蒙版。 如果图层=comp，则在所有缩放后对图层或最终视图图像进行钝化蒙版。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
TQID: 'https://experienceleague.adobe.com/EsklidEmROXoLw9xB1a6qAqTA3Gf3guoUHReqYqXkAo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 144
ht-degree: 2%

---

# op_usmR{#op-usmr}

钝化蒙版。 如果图层=comp，则在所有缩放后对图层或最终视图图像进行钝化蒙版。

这些参数按原样应用，而不管是否已进行降采样。

`op_usmR= *`金额`*[, *`radiusR`*[, *`阈值`*[, *`单色`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">金额</span></span> </p></td> 
  <td class="stentry"> <p>滤镜强度系数（实际0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>滤镜内核半径，以像素为单位（实数0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">阈值</span></span> </p></td> 
  <td class="stentry"> <p>滤镜阈值级别（整数0...255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">单色</span></span> </p></td> 
  <td class="stentry"> <p>设置为0将分别应用至每个颜色组件，或者设置为1将仅应用至图像亮度（强度）。 </p> <p>已忽略灰度图像的<span class="codeph"> <span class="varname">单色</span></span>。 </p> </td> 
 </tr> 
</table>

图层蒙版或复合蒙版也被锐化。

## 属性 {#section-fb5311b34d164946b74dadb32359518a}

图层属性或视图属性。 应用于当前图层或最终视图图像（如果`layer=comp`）。 效果图层忽略它。

## 默认 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0`表示没有钝化蒙版效果。

## 另请参阅 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ， [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ， [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
