---
description: 缩览图类型。 描述如何生成此图像的缩略图。
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# ThumbType{#thumbtype}

缩览图类型。 描述如何生成此图像的缩略图。

支持以下缩略图类型：

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁剪(1) </p></td> 
  <td class="stentry"> <p>将图像裁剪为缩览图长宽比。 除非缩览图矩形和图像的长宽比完全相同，否则图像的一部分会被裁掉，以确保整个缩览图矩形中填充了图像数据。 裁剪矩形使用<span class="codeph">属性：:ThumbHorizAlign</span>和<span class="codeph">属性：:ThumbVertAlign</span>定位到图像中。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>适合(2) </p></td> 
  <td class="stentry"> <p>使整个图像适合缩览图矩形。 图像使用<span class="codeph">属性：:ThumbHorizAlign</span>和<span class="codeph">属性：:ThumbVertAlign</span>定位在缩略图矩形内，并且任何额外空间都填充了<span class="codeph">属性：:ThumbBkgColor</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>纹理(3) </p></td> 
  <td class="stentry"> <p>根据分辨率裁剪图像。 图像按<span class="codeph">目录：:ThumbRes</span>与<span class="codeph">目录：:Resolution</span>的比例缩放。 如果生成的图像大于缩略图，则会裁切图像以适合，如果缩放的图像小于缩略图，则剩余区域将填充<span class="codeph">属性：:ThumbBkgColor</span>。 <span class="codeph"> attribute:::</span> ThumbHorizAlign和 <span class="codeph"> attribute::</span> ThumbVertAlignm用于确定裁剪矩形在较大图像中的位置或缩略图中较小图像的位置。 </p></td> 
 </tr> 
</table>

客户端使用`req=tmb`请求请求图像缩略图。

## 属性 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

枚举值。 有效值为1、2或3，分别对应于“裁剪”、“适合”和“纹理”类型。

## 默认 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` 如果字段不存在，则使用。

## 另请参阅 {#section-fc1a79d3e6274b4381a17da159649a07}

[属性：:AlignType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ，属 [性：:BkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)，属 [性：ThumbHorizColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)，属性 [:ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f) [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69) [](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) [](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) [，目录：AlignCatalog:AlignScaling:AlignCatalog:](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
