---
description: 图层颜色。 指定纯色和效果图层的前景颜色和不透明度，以及文本图层的文本框填充颜色。
seo-description: 图层颜色。 指定纯色和效果图层的前景颜色和不透明度，以及文本图层的文本框填充颜色。
seo-title: 颜色
solution: Experience Manager
title: 颜色
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---


# color{#color}

图层颜色。 指定纯色和效果图层的前景颜色和不透明度，以及文本图层的文本框填充颜色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色  </span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值，带或不带alpha。 </p> </td> 
 </tr> 
</table>

对于图像和文本图层，`color=`将在应用指定颜色*之前填充图层的边界矩形内的透明和半不透明区域。`rotate=``extend=`

## 属性 {#section-d6e74c36a49547849212e4db8927e678}

图层属性。 应用于当前层或层0（如果`layer=comp`）。

*`color`* 假定存在于与像素类型对应的工作颜色空间中 *`color`*。*`color`* 如果图层图像在合并时具有不同的像素类型，则转换精确。

## 默认 {#section-60611c72876b4c45b5c85ce35608e5ec}

纯色和效果图层没有默认值；必须指定颜色。 图像和文本图层默认为0,0,0,0（完全透明）。

## 示例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在以下模板片段中，我们将文本背景设置为50%的不透明颜色，并使用相同的颜色在第2层图像周围添加半透明的10像素边框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另请参阅 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=extend=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)bggc [=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [，色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
