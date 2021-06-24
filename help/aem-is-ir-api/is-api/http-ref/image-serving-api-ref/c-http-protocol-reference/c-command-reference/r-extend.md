---
description: 扩展图层。 向图层添加边距或裁剪图层矩形。
solution: Experience Manager
title: 扩展
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# 扩展{#extend}

扩展图层。 向图层添加边距或裁剪图层矩形。

`extend= *``*, *``*, *``*, *`lefttoprightbottom`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 左、上、下、右</span></span> </p></td> 
  <td class="stentry"> <p>要添加到层矩形(int、int、int、int)的左边、上边、右边和下边（如果值为负）的像素数（或从中删除）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN，topN，bottomN，rightN</span></span> </p></td> 
  <td class="stentry"> <p>要向层矩形的左边、上边、右边和下边添加(或从中移除（如果值为负）的空间量，以相对于原始层矩形的大小（实、实、实、实）的标准化量表示。 </p></td> 
 </tr> 
</table>

`extend=` 在裁剪()图 ** 像后，会将其应用于图层，并且已应用所有图 `crop=` `rotate=`层转换（包括）。

扩展区域填充有`bgColor=`，或者，如果未指定，则保持透明。

在应用了层转换（包括`rotate=`）后，将相对于层矩形的大小，对`extendN=`的参数值进行标准化。

## 属性 {#section-8fc94de871f841f3bf5e1df135972ca9}

层属性。 如果`layer=comp`，则应用于层0。 被效果层忽略。

## 默认 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`，以保持层矩形不变。

## 示例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**裁剪图像，然后添加5像素宽的红色边框：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**将图像缩放为200像素宽度，并将标题文本添加到图像上方的30像素边距中。**

请注意，复合图像的高度会因图像的宽高比而异。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 另请参阅 {#section-2d9572be32ca4602b60920b3810f3638}

[裁剪=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [颜色=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [大小=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [原点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
