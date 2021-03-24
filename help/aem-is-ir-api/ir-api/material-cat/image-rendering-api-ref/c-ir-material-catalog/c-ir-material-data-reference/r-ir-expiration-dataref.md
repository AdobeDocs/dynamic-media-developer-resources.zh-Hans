---
description: 客户端可缓存到实时。 到期前的小时数。 用于管理客户端和代理服务器缓存。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---


# 过期时间{#expiration}

客户端可缓存到实时。 到期前的小时数。 用于管理客户端和代理服务器缓存。

服务器通过将该值添加到传输的时间/日期来计算NTTP响应数据的到期时间/日期。

浏览器使用文件的过期时间管理缓存。 在将请求传递到服务器之前，浏览器将检查其缓存，以查看文件是否已下载。 如果是，并且文件尚未过期，则浏览器将发送条件GET请求（例如，带有If-Modified-Scine HTTP请求标头），而不是普通GET请求。 服务器具有以“304”状态响应而不传输图像的选项。 然后，浏览器将只从其缓存中加载文件。 这可能会显着提高频繁访问数据的整体性能。

服务器会将过期的HTTP响应头设置为当前日期/时间加上最小的晕影：:Expiration and all catalog::Expiration值，用于晕影和渲染操作中涉及的所有材料。

过期时间主要针对图像数据响应进行设置。 某些类型的响应始终会被标记为即时过期（或标记为不可缓存），包括所有错误响应或属性回复。

## 属性 {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

实数、-2、-1、0或更大。 自生成响应图像后到期的小时数。 设置为0可始终立即使响应映像过期，这会有效地禁用客户端缓存。 设置为–1可标记为`never expire`。 在这种情况下，服务器始终返回304状态（未修改）以响应条件`GET`请求，而不检查文件是否实际更改。 设置为–2可使用`attribute::Expiration`提供的默认值。

## 默认 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` 如果字段不存在、值为–2或字段为空，则使用。

## 另请参阅 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[属性：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [晕影：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
