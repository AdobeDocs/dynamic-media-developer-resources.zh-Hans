---
description: 瓦块灌浆颜色和厚度。 模拟陶瓷和天然石砖的浆料。
seo-description: 瓦块灌浆颜色和厚度。 模拟陶瓷和天然石砖的浆料。
seo-title: 灌浆
solution: Experience Manager
title: 灌浆
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# 灌浆{#grout}

瓦块灌浆颜色和厚度。 模拟陶瓷和天然石砖的浆料。

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色  </span> </span> </p> </td> 
  <td class="stentry"> <p>灌浆颜色（灰色或RGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>灌浆厚度；场景坐标单位（通常为英寸）（实数）。 </p> </td> 
 </tr> 
</table>

为最大限度地控制浆料外观，需满足以下要求：

* 拼贴必须是方形或矩形；目前不支持任何其他形状。
* 图像只能包含单个拼贴。
* 图像中的默认灌浆（如果有）在所有四个边上必须具有完全相同的厚度。
* 默认浆料的厚度必须在材料目录(`catalog::GroutWidth`)中指定。

## 属性 {#section-de78b678245b4ffda48097c345949e77}

材料属性。 `*`颜`*` 色必须是RGB颜色值。`*`宽`*` 度必须为实数值0或更大。

如果repeat = 4、5、7、8、9、14或更高，或者为可重复纹理以外的材料指定时，则忽略。

## 默认 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果未指定`grout=`，则不修改图像中的灌浆。 如果指定` grout= *`color`*`，则`*`width`*`默认为`catalog::GroutWidth`。

## 另请参阅 {#section-8d472906a44943f5a8557e98f2fbc71f}

[颜色值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
