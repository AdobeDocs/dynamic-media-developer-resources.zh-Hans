---
description: 图像存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 11%

---

# 存在{#exists}

图像存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一请求标识符

返回名为`catalogRecord.exists`的单个属性。 如果指定的目录条目存在于图像或默认目录中，则属性值将设置为“1”，否则，该属性值将设置为“0”。 `req=exists` 针对上下文 `/is/content` 的请求将指示静态内容目录中是否存在指定的记录。

请求字符串中的其他命令将被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法来指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。只允许使用a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
