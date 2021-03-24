---
description: 这是主日志，用于跟踪向平台服务器发出的所有HTTP请求。 图像渲染（如果启用）会将其访问日志数据写入同一文件。
solution: Experience Manager
title: 访问日志
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# 访问日志{#access-log}

这是主日志，用于跟踪向平台服务器发出的所有HTTP请求。 图像渲染（如果启用）会将其访问日志数据写入同一文件。

访问日志在server.xml中配置。

>[!NOTE]
>
>除了图像服务([!DNL /is/image/*])和图像渲染([!DNL /ir/render/*])的客户端流量外，访问日志还可能包括某些内部流量：访问平台服务器目录系统([!DNL /is-catalog/*])、缓存共享和错误重定向请求([!DNL /is/cache/*])、访问部署到平台服务器的其他包(如Dynamic Media查看器([!DNL /is-viewers/*]))、静态流量和平台服务器服务的静态内容请求(例如[!DNL /is-docs/*])。

根路径为[!DNL /is-catalog]和[!DNL /is/cache]的请求应始终从任何客户端通信分析中排除。
