---
title: 灌浆
description: 图块灌浆颜色和粗细。 模拟陶土和天然石块的灌浆。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
TQID: 'https://experienceleague.adobe.com/FrYxcizVu3nXej1tt4QpX0AsLEylXTfwYRaSQP43HNI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# 灌浆 {#grout}

图块灌浆颜色和粗细。 模拟陶土和天然石块的灌浆。

grout= *`color`*[，*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">颜色</span> </span> </p> </td>
  <td class="stentry"> <p>灌浆颜色（灰色或RGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">宽度</span> </span> </p> </td>
  <td class="stentry"> <p>灌浆厚度；场景坐标单位（通常为英寸）（实际）。 </p> </td>
 </tr> 
</table>

要最大限度地控制灌浆的外观，需要满足以下要求：

* 拼贴必须为正方形或矩形；当前不支持其他形状。
* 图像必须仅包含单个图块。
* 图像中的默认灌注（如果有）必须在所有四条边缘上具有相同的厚度。
* 必须在材料目录(`catalog::GroutWidth`)中指定默认灌浆的厚度。

## 属性 {#section-de78b678245b4ffda48097c345949e77}

材质属性。 `*`color`*`必须是RGB颜色值。 `*`width`*`必须为大于或等于0的实值。

如果重复= 4、5、7、8、9、14或更高，或者为可重复纹理以外的材料指定时，则忽略。

## 默认 {#section-bfab3621f70b4489a21994ab11b20cc6}

如果未指定`grout=`，则不会修改映像中的分组。 如果指定了`grout= *`颜色`*`，则`*`宽度`*`默认为`catalog::GroutWidth`。

## 另请参阅 {#section-8d472906a44943f5a8557e98f2fbc71f}

[颜色值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)

