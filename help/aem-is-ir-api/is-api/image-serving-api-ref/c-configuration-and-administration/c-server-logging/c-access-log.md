---
description: 这是主日志，它跟踪向平台服务器发出的所有HTTP请求。 图像渲染（如果启用）会将其访问日志数据写入同一文件。
seo-description: 这是主日志，它跟踪向平台服务器发出的所有HTTP请求。 图像渲染（如果启用）会将其访问日志数据写入同一文件。
seo-title: 访问日志
solution: Experience Manager
title: 访问日志
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 访问日志{#access-log}

这是主日志，它跟踪向平台服务器发出的所有HTTP请求。 图像渲染（如果启用）会将其访问日志数据写入同一文件。

访问日志在server.xml中配置。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>除了图像服务()和图像渲染( [!DNL /is/image/*])的客户端流量外，访问日志还可能 [!DNL /ir/render/*]包括某些内部流量：访问平台服务器目录系统( [!DNL /is-catalog/*])、缓存共享和错误重定向请求( [!DNL /is/cache/*])、访问部署到平台服务器的其他包，如Scene7查看器( [!DNL /is-viewers/*])、静态流量和由平台服务器服务的静态内容请求(例如， [!DNL /is-docs/*])。

具有和 [!DNL /is-catalog] 根路 [!DNL /is/cache] 径的请求应始终从任何客户端通信分析中排除。
