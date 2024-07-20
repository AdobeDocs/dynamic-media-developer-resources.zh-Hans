---
description: 缩放目标数据。 没有或多个缩放目标属性，这些属性可以与缩放查看器客户端结合使用。
solution: Experience Manager
title: 目标
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# 目标{#targets}

缩放目标数据。 没有或多个缩放目标属性，这些属性可以与缩放查看器客户端结合使用。

服务器在替换“`??`”记录终止符令牌后返回此字段的内容，以响应`req=targets`。

每个缩放目标最多可以关联四个属性：

` Target. *`num`*.frame= *`帧`*`

` Target. *`num`*.rect= *`left，top，width，height`*`

` Target. *`num`*.label= *`标签`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">编号</span> </span> </p> </td> 
  <td class="stentry"> <p>缩放目标编号(int)；缩放目标必须从1开始按顺序连续编号。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">帧</span> </span> </p> </td> 
  <td class="stentry"> <p>用于定位旋转或小册子集的特定帧/页的可选帧/页码；如果未指定用于旋转和小册子查看器，则默认为0；缩放查看器将忽略该值。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">左<span class="varname">，前</span> </span> </p> </td> 
  <td class="stentry"> <p>从图像的左上到缩放目标矩形(int， int)左上角的像素偏移；必须等于或大于0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">宽度，高度</span> </span> </p> </td> 
  <td class="stentry"> <p>缩放目标矩形的像素大小(int， int)；必须大于0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">标签</span> </span> </p> </td> 
  <td class="stentry"> <p>文本数据值；可用作缩放目标链接的文本标签。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">用户数据</span> </span> </p> </td> 
  <td class="stentry"> <p>文本数据值；可用于将特定于目标的信息传递给客户端，例如SKU值或热链接URL。 </p> </td> 
 </tr> 
</table>

目标。 每个缩放目标都需要&#x200B;*`num`*.rect，并且必须在图像内完全指定一个矩形。 所有其他属性都是可选的。

*`label`*&#x200B;和&#x200B;*`userData`*&#x200B;参与文本字符串本地化。 有关详细信息，请参阅&#x200B;*HTTP协议引用*&#x200B;中的[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)。

对于涉及旋转和小册子查看器客户端的应用程序，必须在定义图像集的同一目录记录中定义缩放目标。 查看器将忽略图像集成员的目录记录中的任何缩放目标定义。

Dynamic Media查看器期望全分辨率图像坐标中的缩放目标已由`catalog::Modifier`命令调整。

## 属性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[属性数据](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)值。

## 默认 {#section-feab29f6575e482391086a57f547543c}

无。

## 另请参阅 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[目录：：ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ，[目录：：Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)，[req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)，[文本字符串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
