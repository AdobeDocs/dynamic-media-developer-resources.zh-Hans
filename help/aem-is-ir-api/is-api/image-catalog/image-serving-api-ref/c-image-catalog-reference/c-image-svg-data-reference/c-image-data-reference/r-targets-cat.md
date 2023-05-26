---
description: 缩放目标数据。 没有或多个缩放目标属性，这些属性可以与缩放查看器客户端结合使用。
solution: Experience Manager
title: 目标
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 2%

---

# 目标{#targets}

缩放目标数据。 没有或多个缩放目标属性，这些属性可以与缩放查看器客户端结合使用。

服务器返回此字段的内容以响应 `req=targets`，在替换“ `??`&#39;记录终结器令牌。

每个缩放目标最多可以关联四个属性：

` Target. *`数字`*.frame= *`框架`*`

` Target. *`数字`*.rect= *`left，top，width，height`*`

` Target. *`数字`*.label= *`标签`*`

` Target. *`数字`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 数字 </span> </span> </p> </td> 
  <td class="stentry"> <p>缩放目标编号(int)；缩放目标必须从1开始按顺序连续编号。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 框架 </span> </span> </p> </td> 
  <td class="stentry"> <p>用于定位旋转或小册子集的特定帧/页的可选帧/页码；如果未指定用于旋转和小册子查看器，则默认为0；缩放查看器将忽略该值。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 左，上 </span> </span> </p> </td> 
  <td class="stentry"> <p>从图像的左上角到缩放目标矩形(int， int)左上角的像素偏移；必须为0或更大。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 宽度、高度 </span> </span> </p> </td> 
  <td class="stentry"> <p>缩放目标矩形(int， int)的像素大小；必须大于0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 标签 </span> </span> </p> </td> 
  <td class="stentry"> <p>文本数据值；可用作缩放目标链接的文本标签。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>文本数据值；可用于向客户端传递目标特定信息，例如SKU值或热链接URL。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;每个缩放目标都需要使用.rect，并且必须在图像内完全指定一个矩形。 所有其他属性都是可选的。

*`label`* 和 *`userData`* 参与文本字符串本地化。 请参阅 [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 在 *HTTP协议参考* 了解详细信息。

对于涉及旋转和小册子查看器客户端的应用程序，必须在定义图像集的同一目录记录中定义缩放目标。 查看器将忽略图像集成员的目录记录中的任何缩放目标定义。

Dynamic Media查看器期望全分辨率图像坐标中的缩放目标已由中的命令调整 `catalog::Modifier`.

## 属性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[属性数据](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 值。

## 默认 {#section-feab29f6575e482391086a57f547543c}

无。

## 另请参阅 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog：：图像集](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ， [catalog：：Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)， [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)， [文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
