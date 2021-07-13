---
description: 图像集. 指定在生成req=set响应时使用的图像集值。
solution: Experience Manager
title: imageSet
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# imageSet{#imageset}

图像集. 指定在生成req=set响应时使用的图像集值。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>图像集字符串。 </p></td> 
 </tr> 
</table>

要转义该值并确保任何包含的修饰符未解释为URL查询字符串的一部分，则整个值应以大括号括起来。 如果在净路径中指定了目录记录，则此修改量值将覆盖主记录中的`catalog::ImageSet`。 有关有效图像集语法的说明，请参阅`catalog::ImageSet`文档。

## 属性 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

请求属性。 可选。从主记录覆盖`catalog::ImageSet`。

## 默认 {#section-e8622ff40408450fb79d028f8d37fa6b}

无。

## 示例 {#section-68513d3c601f477399602a0741dab390}

指定要与`req=set`请求一起使用的图像集：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 另请参阅 {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Media Set请求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
