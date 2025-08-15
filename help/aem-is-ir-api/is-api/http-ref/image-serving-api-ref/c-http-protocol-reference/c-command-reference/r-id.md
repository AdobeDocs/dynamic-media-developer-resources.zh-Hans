---
title: id
description: 图像/元数据版本。 处理频繁更改的内容时，缓存网络（如Akamai、浏览器缓存和公司代理服务器缓存）中的服务器可能会存储图像服务响应，这些响应可能会在一段时间内过期。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# id{#id}

图像/元数据版本。 处理频繁更改的内容时，缓存网络（如Akamai、浏览器缓存和公司代理服务器缓存）中的服务器可能会存储图像服务响应，这些响应可能会在一段时间内过期。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>版本字符串。 </p> </td> 
 </tr> 
</table>

图像服务包括版本控制机制，可帮助减少应用程序使用过时的缓存条目的机会。 此机制涉及使用`req=props`获取图像数据和元数据（如图像映射或缩放目标数据）的版本标识符字符串。 然后，使用`id=`命令将版本标识符字符串添加到可缓存的图像服务请求中。

当源图像或元数据更改时，相应的版本ID值也会更改。 通过`id=`命令包含最新的版本ID值可确保不再访问旧的缓存条目。

下表列出了用于每个`req=`类型的版本标识符字符串：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> req=props<b>中的</b>版本标识符 </th> 
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
   <td> <p> 用户数据 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

上面未列出的`req=`类型具有短TTL (`attribute::NonImgExpiration`)，或者它们的响应根本不可缓存；将`id=`包含在此类请求中没有任何优势。

## 属性 {#section-62e973d0d5884abebbb0679f9278ae2c}

请求属性。 可选。 服务器始终忽略。

## 默认 {#section-96136720c82842c89505347ec39e6024}

无。

## 示例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

查看[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)的说明以了解用法示例。

## 另请参阅 {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ， [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)，[目录：：Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)，[属性：：NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
