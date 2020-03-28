---
description: 图像存在。
seo-description: 图像存在。
seo-title: 存在
solution: Experience Manager
title: 存在
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 存在{#exists}

图像存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一请求标识符

Returns a single property named `catalogRecord.exists`. 如果指定的目录条目存在于图像或默认目录中，则该属性值将设置为“1”，否则将设置为“0”。 `req=exists` 针对上下文 `/is/content` 的请求将指示静态内容目录中是否存在指定的记录。

请求字符串中的其他命令将被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

支持JSONP响应格式的请求允许您使用参数的扩展语法指定JS回调处理函数的 `req=` 名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。 仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
