---
title: 灌浆
description: 瓷砖灌浆的颜色和厚度。 模拟陶瓷和天然石砖的灌浆。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# 灌浆 {#grout}

瓷砖灌浆的颜色和厚度。 模拟陶瓷和天然石砖的灌浆。

格劳特= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色 </span> </span> </p> </td>
  <td class="stentry"> <p>灌浆颜色(灰色或RGB)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>灌浆厚度；场景坐标单位（通常为英寸）（实数）。 </p> </td>
 </tr> 
</table>

为了最大限度地控制灌浆外观，需满足以下要求：

* 瓦块必须是正方形或矩形；当前不支持其他形状。
* 图像必须仅包含单个图块。
* 图像中的默认灌浆（如果有）必须在所有四个边缘上具有相同的厚度。
* 必须在材料目录( `catalog::GroutWidth`)。

## 属性 {#section-de78b678245b4ffda48097c345949e77}

材料属性。 `*`颜色`*` 必须是RGB颜色值。 `*`宽度`*` 必须是实际值0或更大。

如果重复= 4、5、7、8、9、14或更高，或者为可重复纹理以外的材料指定时，则忽略。

## 默认 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果 `grout=` 未指定，则不会修改图像中的浆。 如果 `grout= *`颜色`*` 指定， `*`宽度`*` 默认为 `catalog::GroutWidth`.

## 另请参阅 {#section-8d472906a44943f5a8557e98f2fbc71f}

[颜色值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
