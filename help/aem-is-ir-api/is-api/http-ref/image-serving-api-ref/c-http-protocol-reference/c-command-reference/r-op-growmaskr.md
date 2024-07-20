---
title: op_growMaskR
description: 膨胀/腐蚀图像。 对蒙版数据应用形态学膨胀（半径> 0）或腐蚀（半径< 0）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# op_growMaskR{#op-growmaskr}

膨胀/腐蚀图像。 对蒙版数据应用形态学膨胀（半径> 0）或腐蚀（半径&lt; 0）。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>以像素为单位的扩张/侵蚀半径，其中<span class="codeph"><span class="varname"> radiusR</span></span>按原样应用，而不管掩码是否被缩减采样(int -100..100)。 </p></td> 
 </tr> 
</table>

主要用于稍微增大或缩小蒙版，以避免蒙版边缘出现伪像。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

应用于当前图层或图层`0`（如果`layer=comp`）。

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`，无更改。

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
