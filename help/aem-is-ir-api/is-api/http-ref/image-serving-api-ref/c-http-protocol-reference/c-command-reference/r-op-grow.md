---
description: 膨胀/侵蚀图像。 对图像数据应用形态膨胀（半径> 0）或腐蚀（半径< 0）。
solution: Experience Manager
title: op_grow
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---


# op_grow{#op-grow}

膨胀/侵蚀图像。 对图像数据应用形态膨胀（半径> 0）或腐蚀（半径&lt; 0）。

`op_grow= *`半径`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半径</span></span> </p> </td> 
  <td class="stentry"> <p>扩展/侵蚀半径（以像素为单位）（整数–100..100）。 </p></td> 
 </tr> 
</table>

`*`半径`*` （以像素为单位）相对于合成图像。如果图像为颜色，则每个组件都将单独处理。

主要用于修改图层效果的大小。 对于文本图层或带蒙版的纯色图层也有用。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

图层属性。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, for no change.

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
