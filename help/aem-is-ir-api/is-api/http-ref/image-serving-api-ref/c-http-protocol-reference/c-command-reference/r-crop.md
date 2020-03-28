---
description: 裁剪图像。 指定矩形裁剪区域，以像素表示或相对于全分辨率源图像或蒙版图像标准化。
seo-description: 裁剪图像。 指定矩形裁剪区域，以像素表示或相对于全分辨率源图像或蒙版图像标准化。
seo-title: 裁切
solution: Experience Manager
title: 裁切
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 裁切{#crop}

裁剪图像。 指定矩形裁剪区域，以像素表示或相对于全分辨率源图像或蒙版图像标准化。

`crop= *`坐`*, *`标`*`

`cropN= *`coordNsizeN`*, *``*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 坐标</span></span> </p> </td> 
  <td class="stentry"> <p>从源图像的左上角到裁剪矩形的左上角的像素偏移量(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>从源图像的左上角到裁剪矩形的左上角的标准化偏移（实数、实数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小</span></span> </p></td> 
  <td class="stentry"> <p>裁剪矩形的大小（以像素为单位）(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>裁剪矩形相对于源图像大小的标准化大小（实数、实数）。 </p></td> 
 </tr> 
</table>

还可以通过指定负x、y值和／或宽度，高度值大于图像宽度、高度，使图像扩展到其边界之外。 在这种情况下，扩展区域是完全透明的(除非 `bgColor=` 指定)。

## 属性 {#section-632e0405bb9940679b5f8b1c10e0902e}

源图像／蒙版属性。 如果为，则应用于图层0源图像 `layer=comp`。 被未与源图像或蒙版关联的图层忽略。

## 默认 {#section-41f62d386c664f77952bc22e7286bb88}

整个图像( `cropN=0,0,1,1`)。

## 示例 {#section-2c99b481c0a04321979a3b522aa295d1}

**裁切10%左侧和10%右侧：**

`…&cropN=0.1,0,0.8,1&…`

**裁切图像底边20%:**

`…&cropN=0,0,1,0.8&…`

## 另请参阅 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
