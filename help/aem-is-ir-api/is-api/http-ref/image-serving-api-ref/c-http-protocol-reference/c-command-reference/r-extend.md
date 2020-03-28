---
description: 扩展图层。 向图层添加边距或裁切图层矩形。
seo-description: 扩展图层。 向图层添加边距或裁切图层矩形。
seo-title: 扩展
solution: Experience Manager
title: 扩展
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 扩展{#extend}

扩展图层。 向图层添加边距或裁切图层矩形。

`extend= *``*, *``*, *``*, *`左右底部`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>要添加到（如果值为负，则从中删除）图层矩形的左边、上边、右边和下边缘(int、int、int、int)的像素数。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>要向层矩形的左边、上边、右边和下边添加（如果值为负，则从中删除）的空间量，表示为相对于原始层矩形（实、实、实、实）大小的标准化量。 </p></td> 
 </tr> 
</table>

`extend=` 在裁剪()图 *像后* ，将应用到图层，并且已应用所有图层变换(包括 `crop=``rotate=`图层变换)。

扩展区域将填充， `bgColor=`或者，如果未指定，则保持透明。

在应用了 `extendN=` 层变换（包括已应用的层）之后，相对于层矩形的大小，对的参数值进行 `rotate=` 标准化。

## 属性 {#section-8fc94de871f841f3bf5e1df135972ca9}

图层属性。 如果为，则应用于图层0 `layer=comp`。 被效果图层忽略。

## 默认 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`，以保持图层矩形不变。

## 示例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**裁切图像，然后添加5个像素宽的红色边框：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**将图像缩放为200像素宽，并将标题文本添加到图像上方的30像素边距中。**

请注意，复合图像的高度因图像的长宽比而异。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 另请参阅 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , color= [, size=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),来源= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)clipPath [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)[=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
