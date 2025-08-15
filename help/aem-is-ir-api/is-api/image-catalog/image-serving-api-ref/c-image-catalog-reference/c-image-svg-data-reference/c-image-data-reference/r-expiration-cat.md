---
title: 過期
description: 用于管理客户端和代理服务器缓存。 服务器通过将此值与传输时间/日期相加来计算HTTP响应数据的过期时间/日期。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee329834-a2a0-44fd-a0a5-7bf5a8e0a5a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 1%

---

# 過期{#expiration}

用于管理客户端和代理服务器缓存。 服务器通过将此值与传输时间/日期相加来计算HTTP响应数据的过期时间/日期。

浏览器使用文件的过期时间管理缓存。 在将请求传递到服务器之前，浏览器会检查其缓存以查看文件是否已下载。 如果存在，并且文件尚未过期，则浏览器会发送一个有条件的GET请求（例如，在请求标头中设置了If-Modified-Since字段），而不是发送普通的GET请求。 服务器可以选择以“304”状态响应而不传输图像。 然后，浏览器从其缓存加载文件。 这可以显着增加频繁访问数据的总体性能。

“过期”用于以下响应类型：

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

某些类型的响应（例如，错误响应）始终标记为立即过期（或标记为不可缓存），而其他响应（例如，属性或默认图像响应）使用特殊过期设置（`attribute::NonImgExpiration`和`attribute::DefaultExpiration`）。

## 属性 {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

实数、-2、-1或0或更大。 自生成响应图像以来到到期为止的小时数。 设置为0将始终使回复图像立即过期，这样可以有效禁用客户端缓存。 设置为–1以标记为&#x200B;*`never expire`*。 在这种情况下，服务器始终响应有条件的GET请求返回304状态（未修改），而不检查文件是否实际发生了更改。 设置为–2以使用`attribute::Expiration`提供的默认值。

## 默认 {#section-ec72cc1dfc5e4f278174d37da2e39462}

如果字段不存在、值为–2或字段为空，则使用`attribute::Expiration`。

## 另请参阅 {#section-0e5e8595aad641c689726828712a8902}

[attribute：：Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7)，[attribute：：DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)，[attribute：：NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)，[req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
