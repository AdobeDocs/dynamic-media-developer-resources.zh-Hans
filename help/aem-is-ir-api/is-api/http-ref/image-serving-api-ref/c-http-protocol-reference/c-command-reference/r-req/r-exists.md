---
description: 图像存在。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 11%

---


# 存在{#exists}

图像存在。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 唯一请求标识符

返回名为`catalogRecord.exists`的单个属性。 如果指定的目录条目存在于图像或默认目录中，则属性值将设置为&quot;1&quot;，否则将其设置为&quot;0&quot;。 `req=exists` 针对上下文 `/is/content` 的请求将指示静态内容目录中是否存在指定记录。

请求字符串中的其他命令将被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理函数的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
