---
description: 图层颜色。 指定纯色和效果图层的前景色和不透明度，文本框填充文本图层的颜色。
seo-description: 图层颜色。 指定纯色和效果图层的前景色和不透明度，文本框填充文本图层的颜色。
seo-title: 颜色
solution: Experience Manager
title: 颜色
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 3%

---


# color{#color}

图层颜色。 指定纯色和效果图层的前景色和不透明度，文本框填充文本图层的颜色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色  </span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值，带或不带Alpha。 </p> </td> 
 </tr> 
</table>

对于图像和文本图层，`color=`将在应用指定颜色*之前填充图层的边界矩形内的透明和半不透明区域。`rotate=``extend=`

## 属性 {#section-d6e74c36a49547849212e4db8927e678}

图层属性。 应用于当前图层，或应用于`layer=comp`时的图层0。

*`color`* 假定存在于对应于像素类型的工作颜色空间中 *`color`*。*`color`* 如果图层图像在合并时具有不同的像素类型，则会精确转换图像。

## 默认 {#section-60611c72876b4c45b5c85ce35608e5ec}

纯色和效果图层没有默认值；必须指定颜色。 图像和文本图层默认为0,0,0,0（完全透明）。

## 示例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在以下模板片段中，我们将文本背景设置为50%的不透明颜色，并使用相同的颜色在第2层图像周围添加一个半透明的10像素边框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另请参阅 {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [opac=extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),   [bgc](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [=,色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
