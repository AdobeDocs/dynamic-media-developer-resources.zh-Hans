---
description: 過期
solution: Experience Manager
title: 過期
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f51e45fc-fcea-4df6-8c47-e772a1b70a3a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---


# 过期时间{#expiration}

用于管理客户端和代理服务器缓存。 服务器通过将此值添加到传输的时间／日期来计算HTTP响应数据的到期时间／日期。

浏览器使用文件的过期时间管理缓存。 在向服务器传递请求之前，浏览器会检查其缓存，以查看文件是否已下载。 如果是，并且文件尚未过期，则浏览器会发送条件GET请求（例如，在请求标头中设置了If-Modified-Since字段），而不是普通GET请求。 服务器具有以“304”状态进行响应而不传输图像的选项。 然后，浏览器将从其缓存加载文件。 这可以显着提高经常访问数据的整体性能。

过期用于以下响应类型：

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

某些类型的响应（如错误响应）始终被标记为即时过期（或标记为不可缓存），而其他类型（如属性或默认图像响应）则使用特殊的过期设置（`attribute::NonImgExpiration`和`attribute::DefaultExpiration`）。

## 属性 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

实数、-2、-1或0或更大。 生成响应图像后到期的小时数。 设置为0以始终立即使回复图像过期，这会有效地禁用客户端缓存。 设置为-1以标记为&#x200B;*`never expire`*。 在这种情况下，服务器始终会返回304状态（未修改）以响应条件GET请求，而不检查文件是否实际更改。 设置为-2可使用`attribute::Expiration`提供的默认值。

## 默认 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` 如果字段不存在、值为-2或字段为空，则使用。

## 另请参阅 {#section-0e5e8595aad641c689726828712a8902}

[属性：:Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7)，属 [性：:DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)，属 [性：:NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
