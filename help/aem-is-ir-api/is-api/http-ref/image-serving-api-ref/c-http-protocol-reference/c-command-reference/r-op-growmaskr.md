---
description: 膨胀／侵蚀图像。 对蒙版数据应用形态膨胀(radius > 0)或腐蚀(radius < 0)。
seo-description: 膨胀／侵蚀图像。 对蒙版数据应用形态膨胀(radius > 0)或腐蚀(radius < 0)。
seo-title: op_growMaskR
solution: Experience Manager
title: op_growMaskR
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# op_growMaskR{#op-growmaskr}

膨胀／侵蚀图像。 对蒙版数据应用形态膨胀(radius > 0)或腐蚀(radius &lt; 0)。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>无论蒙版是否进行缩减采样(int -100..100)，以像素为单位，其中<span class="codeph"><span class="varname"> radiusR</span></span>按原样应用。 </p></td> 
 </tr> 
</table>

主要用于稍微增大或缩小遮罩以避免遮罩边缘周围出现伪影。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

应用于当前层，如果`layer=comp`，则应用于层`0`。

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, for no change.

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
