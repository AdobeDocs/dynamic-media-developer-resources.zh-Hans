---
description: 图像存在。
seo-description: 图像存在。
seo-title: 存在
solution: Experience Manager
title: 存在
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 12%

---


# 存在{#exists}

图像存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一请求标识符

返回名为`catalogRecord.exists`的单个属性。 如果图像或默认目录中存在指定的目录条目，则属性值将设置为“1”，否则，它将设置为“0”。 `req=exists` 针对上下文 `/is/content` 的请求将指示静态内容目录中是否存在指定记录。

请求字符串中的其他命令将被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
