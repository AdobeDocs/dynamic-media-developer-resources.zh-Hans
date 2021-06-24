---
description: 图像/元数据版本。 当处理频繁更改的内容时，缓存网络（如Akamai、浏览器缓存和公司代理服务器缓存）中的服务器可能会存储一段时间内可能已过期的图像服务响应。
solution: Experience Manager
title: id
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 4%

---

# id{#id}

图像/元数据版本。 当处理频繁更改的内容时，缓存网络（如Akamai、浏览器缓存和公司代理服务器缓存）中的服务器可能会存储一段时间内可能已过期的图像服务响应。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>版本字符串。 </p> </td> 
 </tr> 
</table>

图像提供包括版本控制机制，该机制有助于减少应用程序使用过时的缓存条目的机会。 此机制涉及使用`req=props`获取图像数据和元数据（如图像映射或缩放目标数据）的版本标识符字符串。 然后，使用`id=`命令将版本标识符字符串添加到可缓存的图像服务请求中。

当源图像或元数据发生更改时，相应的版本ID值也会发生更改。 在`id=`命令中包含最新版本id值可确保不再访问旧缓存条目。

下表列出了要用于每种`req=`类型的版本标识符字符串：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req=类型</b> </th> 
   <th class="entry"> <b> req=props中的版本标识符</b> </th> 
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
   <td> <p> 蒙版 </p> </td> 
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
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` 以上未列出的类型的TTL( `attribute::NonImgExpiration`)较短，或者其响应根本不可缓存；在此类请求中包含 `id=` 没有任何优势。

## 属性 {#section-62e973d0d5884abebbb0679f9278ae2c}

请求属性。 可选。服务器始终忽略。

## 默认 {#section-96136720c82842c89505347ec39e6024}

无。

## 示例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

有关用法的示例，请参阅[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)的说明。

## 另请参阅 {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
