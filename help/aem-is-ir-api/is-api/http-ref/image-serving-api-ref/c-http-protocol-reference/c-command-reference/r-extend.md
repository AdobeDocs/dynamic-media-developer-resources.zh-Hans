---
description: 扩展图层。 向图层添加边距或裁切图层矩形。
solution: Experience Manager
title: 扩展
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# extend{#extend}

扩展图层。 向图层添加边距或裁切图层矩形。

`extend= *`左`*, *``*, *``*, *`右底`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left，top，bottom，right</span></span> </p></td> 
  <td class="stentry"> <p>要添加到（如果值为负，则从中删除）图层矩形的左边、上边、右边和下边(int、int、int、int)的像素数。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN，topN，bottomN，rightN</span></span> </p></td> 
  <td class="stentry"> <p>要添加到（或从中删除，如果值为负）图层矩形的左边、上边、右边和下边的空间量，表示为相对于原始图层矩形（实、实、实、实）大小的标准化量。 </p></td> 
 </tr> 
</table>

`extend=` 在裁剪()图 ** 像并应用所有图 `crop=`层变换(包括 `rotate=`图层变换)后应用。

扩展区域用`bgColor=`填充，或者，如果未指定，则保持透明。

在应用了`rotate=`等图层变换后，将相对于图层矩形的大小标准化`extendN=`的参数值。

## 属性 {#section-8fc94de871f841f3bf5e1df135972ca9}

图层属性。 如果`layer=comp`，则应用于层0。 被效果图层忽略。

## 默认 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`，以便不更改图层矩形。

## 示例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**裁剪图像，然后添加5个像素宽的红色边框：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**将图像缩放为200像素宽，并将标题文本添加到图像上方30像素边距中。**

请注意，复合图像的高度会因图像的长宽比而不同。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 另请参阅 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , color= [, size](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)= [, 来源](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138) [Path=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
