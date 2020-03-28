---
description: 缩略图类型。 描述如何生成此图像的缩略图。
seo-description: 缩略图类型。 描述如何生成此图像的缩略图。
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbType{#thumbtype}

缩略图类型。 描述如何生成此图像的缩略图。

支持以下缩略图类型：

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁剪(1) </p></td> 
  <td class="stentry"> <p>将图像裁切为缩览图长宽比。 除非缩略图矩形和图像的长宽比完全相同，否则图像的一部分会被裁掉，以确保整个缩略图矩形中填充了图像数据。 裁切矩形使用属性：:ThumbHorizAlign <span class="codeph"> 和属性</span> : <span class="codeph"> ThumbVertAlign在图像中定位</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>适合(2) </p></td> 
  <td class="stentry"> <p>使整个图像适合缩览图矩形。 图像使用属性：:ThumbHorizAlign <span class="codeph"> and</span> attribute::ThumbVertAlign <span class="codeph"> ，在缩略图矩形内放置图像，并且任何额外的空间都填充了属性：</span>:ThumbBkgColor <span class="codeph"></span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>纹理(3) </p></td> 
  <td class="stentry"> <p>根据分辨率裁剪图像。 图像按目录：:ThumbRes <span class="codeph"> 与目录</span> : <span class="codeph"> Resolution的比例缩放</span>。 如果生成的图像大于缩略图，则会裁切该图像以适合，如果缩放的图像小于缩略图，则剩余区域将填充以下属 <span class="codeph"> 性：:ThumbBkgColor</span>。 <span class="codeph"> 属性：:ThumbHorizAlign</span> and <span class="codeph"></span> attribute::ThumbVertAlign用于确定裁剪矩形在较大图像中的位置或缩略图中较小图像的位置。 </p></td> 
 </tr> 
</table>

客户端请求带有请求的图像缩 `req=tmb` 略图。

## 属性 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

枚举值。 有效值为1、2或3，分别对应于“裁剪”、“适合”和“纹理”类型。

## 默认 {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` 如果字段不存在，则使用该字段。

## 另请参阅 {#section-fc1a79d3e6274b4381a17da159649a07}

[属性：:Attribute::BType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) , [属性：:BKgAttribut属性：HHzZ](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)属性： [AlignVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)[](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)[](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[，目录：ResResHalignAdobertCatalog:AlignShomb，属性缩略图：](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
