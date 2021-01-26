---
description: 图像／元数据版本。 当处理频繁更改的内容时，缓存网络（如Akamai、浏览器缓存和公司代理服务器缓存）中的服务器可以存储可能过时的图像服务响应。
seo-description: 图像／元数据版本。 当处理频繁更改的内容时，缓存网络（如Akamai、浏览器缓存和公司代理服务器缓存）中的服务器可以存储可能过时的图像服务响应。
seo-title: id
solution: Experience Manager
title: id
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 4%

---


# id{#id}

图像／元数据版本。 当处理频繁更改的内容时，缓存网络（如Akamai、浏览器缓存和公司代理服务器缓存）中的服务器可以存储可能过时的图像服务响应。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>版本字符串。 </p> </td> 
 </tr> 
</table>

图像服务包括版本控制机制，它有助于减少应用程序使用过时的缓存条目的可能性。 此机制涉及使用`req=props`获取图像数据和元数据(如图像映射或缩放目标数据)的版本标识符字符串。 然后，使用`id=`命令将版本标识符字符串添加到可缓存的图像服务请求中。

当源图像或元数据发生更改时，相应的版本ID值也将发生更改。 在`id=`命令中包含一个最新版本id值，可确保不再访问旧缓存条目。

下表列表了要用于每种`req=`类型的版本标识符字符串：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req=类型</b> </th> 
   <th class="entry"> <b> req=props的版本标识符</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 地图 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 遮罩 </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 目标 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 用户数据 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` 以上未列出的类型的TTL短() `attribute::NonImgExpiration`或其响应根本无法缓存；包含此类请求 `id=` 没有优势。

## 属性 {#section-62e973d0d5884abebbb0679f9278ae2c}

请求属性。 可选。服务器始终忽略。

## 默认 {#section-96136720c82842c89505347ec39e6024}

无。

## 示例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

例如，请参见[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)的说明。

## 另请参阅 {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), catalog::Expiration [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) [属性：:NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
