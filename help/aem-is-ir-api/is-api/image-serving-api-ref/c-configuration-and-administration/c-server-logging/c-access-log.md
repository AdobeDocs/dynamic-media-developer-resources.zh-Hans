---
description: 这是主日志，用于跟踪向Platform Server发出的所有HTTP请求。 如果启用，图像渲染会将其访问日志数据写入同一文件。
solution: Experience Manager
title: 访问日志
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# 访问日志{#access-log}

这是主日志，用于跟踪向Platform Server发出的所有HTTP请求。 如果启用，图像渲染会将其访问日志数据写入同一文件。

访问日志在server.xml中配置。

>[!NOTE]
>
>除了用于图像服务([!DNL /is/image/*])和图像渲染([!DNL /ir/render/*])的客户端流量之外，访问日志还可能包含某些内部流量：访问Platform Server目录系统([!DNL /is-catalog/*])、缓存共享和错误重定向请求([!DNL /is/cache/*])、访问部署到Platform Server的其他包(如Dynamic Media查看器([!DNL /is-viewers/*]))、静态流量和平台服务器服务的静态内容请求(例如，[!DNL /is-docs/*])。

根路径为[!DNL /is-catalog]和[!DNL /is/cache]的请求应始终从任何客户端流量分析中排除。
