---
title: 扩展
description: 扩展层。 向图层添加边距或裁切图层矩形。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# 扩展{#extend}

扩展层。 向图层添加边距或裁切图层矩形。

`extend= *`左`*, *`上`*, *`右`*, *`下`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">左、上、下、右</span></span> </p></td> 
  <td class="stentry"> <p>要添加到图层矩的左边缘、上边缘、右边缘和下边缘(int、int、int、int、int)的像素数（如果值为负值，则从中移除像素数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN，topN，bottomN，rightN</span></span> </p></td> 
  <td class="stentry"> <p>要添加到（或从中删除，如果该值为负）图层矩形的左边缘、上边缘、右边缘和下边缘的空间量，以相对于原始图层矩大小（实数、实数、实数、实数）的规范化数量表示。 </p></td> 
 </tr> 
</table>

在`extend=`之后将&#x200B;*应用于图层*&#x200B;将裁剪图像(`crop=`)，并且已应用所有图层转换，包括`rotate=`。

扩展区域已填充`bgColor=`，如果未指定，则保持透明。

在应用层转换（包括`extendN=`）之后，`rotate=`的参数值将相对于层矩形的大小进行标准化。

## 属性 {#section-8fc94de871f841f3bf5e1df135972ca9}

层属性。 应用于图层0（如果`layer=comp`）。 被效果层忽略。

## 默认 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`，表示图层矩形未发生更改。

## 示例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**裁切图像，然后添加5像素宽的红色边框：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**将图像缩放到200像素的宽度，并将标题文本添加到图像上方的30像素边距。**

请注意，复合图像的高度会因图像的纵横比而异。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 另请参阅 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ， [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)， [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)， [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
