---
description: 预载服务器缓存。 执行请求的方式与req=img类似，但服务器返回的是返回图像的长度(image.length)，格式为MIME类型为text/plain的文本数据。
seo-description: 预载服务器缓存。 执行请求的方式与req=img类似，但服务器返回的是返回图像的长度(image.length)，格式为MIME类型为text/plain的文本数据。
seo-title: 加载缓存
solution: Experience Manager
title: 加载缓存
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44f0db05-2323-4aa2-853c-f78e656a4308
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# loadcache{#loadcache}

预载服务器缓存。 执行请求的方式与req=img类似，但服务器返回的是返回图像的长度(image.length)，格式为MIME类型为text/plain的文本数据。

`req=loadcache`

HTTP响应不可缓存。

请求中的其他命令将按文档进行应用。
