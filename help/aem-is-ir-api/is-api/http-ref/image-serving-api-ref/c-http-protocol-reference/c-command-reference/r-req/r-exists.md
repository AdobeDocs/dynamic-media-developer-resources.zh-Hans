---
description: 存在图像。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# 存在{#exists}

存在图像。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一请求标识符

返回名为的单个属性 `catalogRecord.exists`. 如果指定的目录条目存在于图像或默认目录中，则属性值设置为“1”，否则设置为“0”。 `req=exists` 针对的请求 `/is/content` 上下文将指示静态内容目录中是否存在指定记录。

请求字符串中的其他命令将被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

支持JSONP响应格式的请求允许您使用扩展语法指定JS回调处理程序的名称 `req=` 参数：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。 仅允许a-z、A-Z和0-9字符。 可选. 默认值为 `s7jsonResponse`.
