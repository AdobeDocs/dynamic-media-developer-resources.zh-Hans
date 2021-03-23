---
description: 瓦块灌浆颜色和厚度。 模拟陶瓷和天然石砖的灌浆。
seo-description: 瓦块灌浆颜色和厚度。 模拟陶瓷和天然石砖的灌浆。
seo-title: 灌浆
solution: Experience Manager
title: 灌浆
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# wray{#grout}

瓦块灌浆颜色和厚度。 模拟陶瓷和天然石砖的灌浆。

gruet= *`color`*[,*`width`*]

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

为最大限度地控制灌浆外观，需满足以下要求：

* 拼贴必须是方形或矩形；此时不支持其他形状。
* 图像只能包含单个拼贴。
* 图像中的默认灌浆（如果有）必须在所有四条边上具有完全相同的厚度。
* 必须在材料目录(`catalog::GroutWidth`)中指定默认灌浆厚度。

## 属性 {#section-de78b678245b4ffda48097c345949e77}

材料属性。 `*`颜`*` 色必须是RGB颜色值。`*`宽`*` 度必须是实值0或更大。

如果repeat = 4、5、7、8、9、14或更高，或者为可重复纹理以外的材料指定时，则忽略。

## 默认 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果未指定`grout=`，则不修改图像中的灌浆。 如果指定` grout= *`color`*`，则`*`width`*`默认为`catalog::GroutWidth`。

## 另请参阅 {#section-8d472906a44943f5a8557e98f2fbc71f}

[颜色值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
