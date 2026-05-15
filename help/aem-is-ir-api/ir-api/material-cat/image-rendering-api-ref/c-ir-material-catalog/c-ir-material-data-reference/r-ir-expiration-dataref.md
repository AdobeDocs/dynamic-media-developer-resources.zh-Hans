---
title: 過期
description: 客户端缓存生存时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
TQID: 'https://experienceleague.adobe.com/dFnSsD8mmC0aPefS3Z0GujF1A-p1nCQyiNpzMXxOBEQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# 過期{#expiration}

客户端缓存生存时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。

服务器通过将此值与传输时间/日期相加来计算NTTP响应数据的过期时间/日期。

浏览器使用文件的过期时间管理缓存。 在将请求传递到服务器之前，浏览器会检查其缓存，以查看文件是否已下载。 如果存在，并且文件尚未过期，则浏览器会发送一个有条件的GET请求（例如，使用If-Modified-Since HTTP请求标头），而不是发送普通的GET请求。 服务器可以选择以“304”状态响应而不传输图像。 然后，浏览器只需从其缓存加载文件即可。 这可以显着增加频繁访问数据的总体性能。

服务器将expires HTTP响应标头设置为当前日期/时间加上晕影：：Expiration和所有catalog：：Expiration值中的最小值，该值适用于渲染操作中涉及到的晕影和所有材料。

过期时间主要针对图像数据响应而设置。 某些类型的响应始终标记为立即过期（或标记为不可缓存），包括所有错误响应或属性回复。

## 属性 {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

实数、-2、-1、0或更大。 自生成响应图像以来到到期为止的小时数。 设置为0将始终使响应映像立即过期，这样可以有效禁用客户端缓存。 设置为–1以标记为`never expire`。 在这种情况下，服务器始终返回304状态（未修改）以响应条件`GET`请求，而不检查文件是否实际发生了更改。 设置为–2以使用`attribute::Expiration`提供的默认值。

## 默认 {#section-79d71706e12a4493a69d7febc3a1f271}

如果字段不存在、值为–2或字段为空，则使用`attribute::Expiration`。

## 另请参阅 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[属性：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ， [晕影：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)，[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
