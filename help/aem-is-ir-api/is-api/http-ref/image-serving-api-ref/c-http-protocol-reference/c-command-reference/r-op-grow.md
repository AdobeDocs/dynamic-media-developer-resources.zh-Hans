---
title: op_grow
description: 膨胀/腐蚀图像。 对图像数据应用形态学膨胀（半径> 0）或腐蚀（半径< 0）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 2%

---

# op_grow{#op-grow}

膨胀/腐蚀图像。 对图像数据应用形态学膨胀（半径> 0）或腐蚀（半径&lt; 0）。

`op_grow= *`半径`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半径</span></span> </p> </td> 
  <td class="stentry"> <p>扩张/侵蚀半径，以像素为单位(int -100..100)。 </p></td> 
 </tr> 
</table>

`*`半径`*` 以相对于复合图像的像素为单位。 如果图像是彩色的，则每个组件单独进行处理。

主要用于修改图层效果的大小。 在文本图层或带蒙版的纯色图层上实现特殊效果也很有用。

## 属性 {#section-b1c66d65168d4ea695e8662ea690bd4e}

层属性。 应用到当前图层或复合图像，如果 `layer=comp`.

## 默认 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`，表示无更改。

## 另请参阅 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[图层效果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
