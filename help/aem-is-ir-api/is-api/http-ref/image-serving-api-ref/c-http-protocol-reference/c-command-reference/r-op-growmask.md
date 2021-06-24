---
description: 膨胀/腐蚀图像。 对蒙版数据应用形态膨胀（半径> 0）或腐蚀（半径< 0）。
solution: Experience Manager
title: op_growMask
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# op_growMask{#op-growmask}

膨胀/腐蚀图像。 对蒙版数据应用形态膨胀（半径> 0）或腐蚀（半径&lt; 0）。

`op_growMask= *`半径`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半径</span> </p> </td> 
  <td class="stentry"> <p>以像素为单位，展开/侵蚀半径，其中半径假定应用于全分辨率蒙版，因此缩小采样掩码的半径(int -100.100)。 </p></td> 
 </tr> 
</table>

主要用于稍微增大或收缩蒙版以避免蒙版边缘周围出现伪影。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

应用于当前层，如果`layer=comp`，则应用于`0`层。

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`，无更改。

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
