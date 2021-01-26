---
description: 图像（默认）。 请求标准图像数据。
seo-description: 图像（默认）。 请求标准图像数据。
seo-title: img
solution: Experience Manager
title: img
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 20%

---


# img{#img}

图像（默认）。 请求标准图像数据。

`req=img`

回复数据格式和响应MIME类型由`fmt=`确定。 `req=img` 是默认请求类型，无需明确指定。HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

其他请求命令将按说明进行应用。
