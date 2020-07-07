---
description: 这是主日志，用于跟踪向平台服务器发出的所有HTTP请求。 如果启用图像渲染，则将其访问日志数据写入同一文件。
seo-description: 这是主日志，用于跟踪向平台服务器发出的所有HTTP请求。 如果启用图像渲染，则将其访问日志数据写入同一文件。
seo-title: 访问日志
solution: Experience Manager
title: 访问日志
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# 访问日志{#access-log}

这是主日志，用于跟踪向平台服务器发出的所有HTTP请求。 如果启用图像渲染，则将其访问日志数据写入同一文件。

访问日志在server.xml中配置。

>[!NOTE]
>
>除了图像服务()和图像渲染() [!DNL /is/image/*]的客户端流量外，访 [!DNL /ir/render/*]问日志还可能包括某些内部流量： 访问平台服务器目录系统( [!DNL /is-catalog/*])、缓存共享和错误重定向请求( [!DNL /is/cache/*])、访问部署到平台服务器的其他包(如Scene7查看器( [!DNL /is-viewers/*])、静态通信和平台服务器服务的静态内容请求(如 [!DNL /is-docs/*])。

具有和根 [!DNL /is-catalog] 路径 [!DNL /is/cache] 的请求应始终从任何客户端通信分析中排除。
