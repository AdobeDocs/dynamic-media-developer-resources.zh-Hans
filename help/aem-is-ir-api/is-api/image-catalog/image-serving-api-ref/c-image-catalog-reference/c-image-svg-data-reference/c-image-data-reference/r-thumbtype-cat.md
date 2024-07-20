---
description: 缩略图类型。 描述如何生成此图像的缩略图。
solution: Experience Manager
title: 缩略图类型
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a90b587d-6893-44e4-8dce-7676bc7eebe3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# 缩略图类型{#thumbtype}

缩略图类型。 描述如何生成此图像的缩略图。

支持以下缩略图类型：

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>裁切(1) </p></td> 
  <td class="stentry"> <p>将图像裁剪为缩略图纵横比。 除非缩略图矩形和图像的长宽比完全相同，否则将裁切图像的部分内容，以确保使用图像数据填充整个缩略图矩形。 使用<span class="codeph">属性：：ThumbHorizAlign</span>和<span class="codeph">属性：：ThumbVertAlign</span>将裁切矩形放置在图像中。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>适合(2) </p></td> 
  <td class="stentry"> <p>将整个图像调整到缩略图矩形中。 使用<span class="codeph">属性：：ThumbHorizAlign</span>和<span class="codeph">属性：：ThumbVertAlign</span>将图像定位在缩略图矩形内，并且任何额外的空格都使用<span class="codeph">属性：：ThumbBkgColor</span>填充。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>纹理(3) </p></td> 
  <td class="stentry"> <p>根据分辨率裁切图像。 图像按<span class="codeph"> catalog：：ThumbRes</span>与<span class="codeph"> catalog：：Resolution</span>的比例缩放。 如果结果图像大于缩略图，则会裁剪图像以适合图像；如果缩放图像小于缩略图，则剩余区域将使用<span class="codeph">属性：：ThumbBkgColor</span>填充。 <span class="codeph"> attribute：：ThumbHorizAlign</span>和<span class="codeph"> attribute：：ThumbVertAlign</span>用于确定裁切矩形在较大图像中的位置或较小图像在缩略图中的位置。 </p></td> 
 </tr> 
</table>

客户端通过`req=tmb`请求来请求图像缩略图。

## 属性 {#section-c58a8e67c2134ca3a0edd21b20dd3052}

枚举值。 有效值为1、2或3，分别对应于“裁切”、“适合”和“纹理”类型。

## 默认 {#section-a6a7c43a83384a4aab861a48d73c7c26}

如果字段不存在、值为0或字段为空，则使用`attribute::ThumbType`。

## 另请参阅 {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute：：ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ，[attribute：：ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e)，[attribute：：ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691)，[attribute：：ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f)，[catalog：：ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)，[catalog：：Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)，[req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)，[缩略图缩放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
