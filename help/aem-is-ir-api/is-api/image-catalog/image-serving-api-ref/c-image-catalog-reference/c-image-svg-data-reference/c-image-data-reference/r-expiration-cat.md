---
description: 過期
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ee329834-a2a0-44fd-a0a5-7bf5a8e0a5a5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# 過期{#expiration}

用于管理客户端和代理服务器缓存。 服务器通过将此值添加到传输的时间/日期来计算HTTP响应数据的过期时间/日期。

浏览器使用文件的过期时间来管理缓存。 在向服务器传递请求之前，浏览器会检查其缓存，以查看文件是否已下载。 如果是，并且文件尚未过期，则浏览器会发送一个条件GET请求（例如，在请求标头中设置了If-Modified-Since字段），而不是常规GET请求。 服务器可以选择以“304”状态响应，而不发送图像。 然后，浏览器从其缓存中加载文件。 这可能会显着提高频繁访问数据的整体性能。

以下响应类型将使用过期时间：

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

某些类型的响应（例如错误响应）始终被标记为立即过期（或标记为不可缓存），而其他类型的响应（例如属性或默认图像响应）则使用特殊的过期设置（`attribute::NonImgExpiration`和`attribute::DefaultExpiration`）。

## 属性 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

实数、-2、-1或0或更大。 自生成响应图像后到期的小时数。 设置为0时，将始终立即使回复图像过期，这会有效地禁用客户端缓存。 设置为–1可标记为&#x200B;*`never expire`*。 在这种情况下，服务器始终在响应条件GET请求时返回304状态（未修改），而不检查文件是否实际发生更改。 设置为–2时，将使用`attribute::Expiration`提供的默认值。

## 默认 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` 如果字段不存在，则当值为–2或字段为空时，将使用。

## 另请参阅 {#section-0e5e8595aad641c689726828712a8902}

[属性：:Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [属性：:DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [属性：:NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
