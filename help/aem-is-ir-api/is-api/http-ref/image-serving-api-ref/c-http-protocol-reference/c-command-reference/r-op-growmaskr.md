---
description: 膨胀/腐蚀图像。 对蒙版数据应用形态膨胀（半径> 0）或腐蚀（半径< 0）。
solution: Experience Manager
title: op_growMaskR
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# op_growMaskR{#op-growmaskr}

膨胀/腐蚀图像。 对蒙版数据应用形态膨胀（半径> 0）或腐蚀（半径&lt; 0）。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>扩展/腐蚀半径（以像素为单位），其中<span class="codeph"><span class="varname"> radiusR</span></span>按原样应用，而不考虑蒙版是否采样缩减(int -100..100)。 </p></td> 
 </tr> 
</table>

主要用于稍微增大或收缩蒙版以避免蒙版边缘周围出现伪影。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

应用于当前层，如果`layer=comp`，则应用于`0`层。

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`，无更改。

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
