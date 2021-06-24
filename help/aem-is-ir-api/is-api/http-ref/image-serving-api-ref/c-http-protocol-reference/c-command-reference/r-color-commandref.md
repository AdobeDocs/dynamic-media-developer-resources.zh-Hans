---
description: 图层颜色。 指定实色和效果图层的前景颜色和不透明度，并为文本图层填充文本框颜色。
solution: Experience Manager
title: 颜色
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 4%

---

# 颜色{#color}

图层颜色。 指定实色和效果图层的前景颜色和不透明度，并为文本图层填充文本框颜色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色  </span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值，带或不带Alpha。 </p> </td> 
 </tr> 
</table>

对于图像和文本层，`color=`在应用`rotate=`和`extend=`之前，用指定颜色*填充层的边界矩形内的透明和半不透明区域。

## 属性 {#section-d6e74c36a49547849212e4db8927e678}

层属性。 在`layer=comp`时应用于当前层或应用于层0。

*`color`* 假定存在于对应于像素类型的工作颜色空间中 *`color`*。*`color`* 如果层图像在合并时具有不同的像素类型，则精确地转换。

## 默认 {#section-60611c72876b4c45b5c85ce35608e5ec}

实色和效果层没有缺省值；必须指定颜色。 对于图像和文本层，默认为0,0,0,0（完全透明）。

## 示例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在以下模板片段中，我们将文本背景设置为50%不透明的颜色，并使用相同的颜色在第2层图像周围添加一个半透明的10像素边框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另请参阅 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
