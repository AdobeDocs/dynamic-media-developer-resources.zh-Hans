---
description: 图像（默认）。 请求标准图像数据。
seo-description: 图像（默认）。 请求标准图像数据。
seo-title: img
solution: Experience Manager
title: img
topic: Scene7 Image Serving - Image Rendering API
uuid: 4809f916-0ccf-4a24-a93b-c51ed6203061
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# img{#img}

图像（默认）。 请求标准图像数据。

`req=img`

回复数据格式和响应MIME类型由决定 `fmt=`。 `req=img` 是默认的请求类型，无需明确指定。 HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

其他请求命令将按说明应用。
