---
description: 膨胀/侵蚀图像。 对蒙版数据应用形态膨胀(radius > 0)或腐蚀(radius < 0)。
solution: Experience Manager
title: op_growMask
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# op_growMask{#op-growmask}

膨胀/侵蚀图像。 对蒙版数据应用形态膨胀(radius > 0)或腐蚀(radius &lt; 0)。

`op_growMask= *`半径`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半径</span> </p> </td> 
  <td class="stentry"> <p>扩大/侵蚀半径（以像素为单位），其中假定半径应用于全分辨率蒙版，因此缩小取样缩小蒙版(int -100.100)。 </p></td> 
 </tr> 
</table>

主要用于稍微增大或缩小蒙版以避免蒙版边缘周围出现伪影。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

应用于当前图层，或应用于`layer=comp`的图层`0`。

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, for no change.

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
