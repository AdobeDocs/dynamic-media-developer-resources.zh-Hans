---
title: 裁切
description: 裁切图像。 指定矩形裁剪区域，以像素表示或相对于全分辨率源图像或蒙版图像规范化。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# 裁切{#crop}

裁切图像。 指定矩形裁剪区域，以像素表示或相对于全分辨率源图像或蒙版图像规范化。

`crop= *`列`*, *`大小`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">顺序</span></span> </p> </td> 
  <td class="stentry"> <p>从源图像的左上角到裁切矩形左上角的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>从源图像的左上角到裁切矩形左上角的标准化偏移（实际、实际）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">大小</span></span> </p></td> 
  <td class="stentry"> <p>裁切矩形的大小，以像素(int， int)为单位。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">大小N</span></span> </p></td> 
  <td class="stentry"> <p>相对于源图像大小（实数、实数）的裁切矩形的标准化大小。 </p></td> 
 </tr> 
</table>

还可以通过指定大于图像宽度、高度的负x、y值和/或宽度、高度值来将图像延伸到其边界之外。 在这种情况下，扩展区域是完全透明的（除非指定了`bgColor=`）。

## 属性 {#section-632e0405bb9940679b5f8b1c10e0902e}

Source图像/蒙版属性。 应用于0层源图像（如果`layer=comp`）。 被与源图像或蒙版无关的图层忽略。

## 默认 {#section-41f62d386c664f77952bc22e7286bb88}

整个图像(`cropN=0,0,1,1`)。

## 示例 {#section-2c99b481c0a04321979a3b522aa295d1}

**裁切左侧的10%折扣和右侧的10%折扣：**

`…&cropN=0.1,0,0.8,1&…`

**裁切比图像下边缘低20%的内容：**

`…&cropN=0,0,1,0.8&…`

## 另请参阅 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ， [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)， [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
