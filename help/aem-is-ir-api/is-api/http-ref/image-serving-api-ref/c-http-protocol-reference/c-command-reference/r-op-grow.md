---
description: 膨胀／侵蚀图像。 对图像数据应用形态膨胀(radius > 0)或腐蚀(radius < 0)。
seo-description: 膨胀／侵蚀图像。 对图像数据应用形态膨胀(radius > 0)或腐蚀(radius < 0)。
seo-title: op_grow
solution: Experience Manager
title: op_grow
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bc9bf889-f7e1-4a65-b6d6-7e1257ef8c11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# op_grow{#op-grow}

膨胀／侵蚀图像。 对图像数据应用形态膨胀(radius > 0)或腐蚀(radius &lt; 0)。

`op_grow= *`半径`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半径</span></span> </p> </td> 
  <td class="stentry"> <p>以像素为单位的扩展／腐蚀半径(int -100..100)。 </p></td> 
 </tr> 
</table>

`*`辐`*` 度（以像素为单位）相对于复合图像。如果图像为颜色，则每个组件将单独处理。

主要用于修改图层效果的大小。 对于文本图层或带有蒙版的纯色图层，也有用于实现特殊效果。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

图层属性。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, for no change.

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
