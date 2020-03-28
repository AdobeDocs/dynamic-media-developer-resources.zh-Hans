---
description: 缩放目标数据。 无或更多缩放目标属性，这些属性可与缩放查看器客户端一起使用。
seo-description: 缩放目标数据。 无或更多缩放目标属性，这些属性可与缩放查看器客户端一起使用。
seo-title: 目标
solution: Experience Manager
title: 目标
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# 目标{#targets}

缩放目标数据。 无或更多缩放目标属性，这些属性可与缩放查看器客户端一起使用。

在替换“ ”记录终结器令牌后，服务 `req=targets`器返回此字段 `??`的内容。

最多四个属性可以与每个缩放目标关联：

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *`numuserData`*.userData= *``*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 数字 </span></span> </p> </td> 
  <td class="stentry"> <p>缩放目标号(int);缩放目标必须从1开始按顺序和连续进行编号。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 帧 </span></span> </p> </td> 
  <td class="stentry"> <p>可选的帧／页码，用于定位旋转或小册子集的特定帧／页；如果未为旋转和小册子查看器的使用指定值，则默认为0;被缩放查看器忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 左，上 </span></span> </p> </td> 
  <td class="stentry"> <p>从图像左上角到缩放目标矩形左上角的像素偏移量(int, int);必须为0或更大。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 宽度，高度 </span></span> </p> </td> 
  <td class="stentry"> <p>缩放目标矩形的像素大小(int, int);必须大于0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 标签 </span></span> </p> </td> 
  <td class="stentry"> <p>文本数据值；可用作缩放目标链接的文本标签。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 用 <span class="varname"> 户数据 </span></span> </p> </td> 
  <td class="stentry"> <p>文本数据值；可用于将目标特定信息传递给客户端，如SKU值或热链接URL。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;每个缩放目标都需要。rect，并且必须在图像中完全指定一个矩形。 所有其他属性都是可选的。

*`label`* 并参 *`userData`* 与文本字符串本地化。 有关详细 [信息，请参阅](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)*HTTP协议参考中的文本字符串本地化* 。

对于涉及旋转和小册子查看器客户端的应用程序，缩放目标必须在定义图像集的同一目录记录中定义。 查看器将忽略图像集成员的目录记录中的任何缩放目标定义。

Scene7查看器期望在已通过命令调整的全分辨率图像坐标中实现缩放目标 `catalog::Modifier`。

## 属性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[属性数据](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 值。

## 默认 {#section-feab29f6575e482391086a57f547543c}

无。

## 另请参阅 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog:::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text String本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
