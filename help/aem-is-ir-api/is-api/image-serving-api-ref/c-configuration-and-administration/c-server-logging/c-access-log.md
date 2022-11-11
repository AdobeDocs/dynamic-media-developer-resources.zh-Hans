---
description: 这是主日志，用于跟踪对 [!DNL Platform Server]. 如果启用，图像渲染会将其访问日志数据写入同一文件。
solution: Experience Manager
title: 访问日志
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 访问日志{#access-log}

这是主日志，用于跟踪对 [!DNL Platform Server]. 如果启用，图像渲染会将其访问日志数据写入同一文件。

访问日志在server.xml中配置。

>[!NOTE]
>
>除了图像服务的客户端流量( [!DNL /is/image/*])和图像渲染( [!DNL /ir/render/*])，访问日志可能包含某些内部流量：对 [!DNL Platform Server] 目录系统( [!DNL /is-catalog/*])、缓存共享和错误重定向请求( [!DNL /is/cache/*])，访问部署到的其他包 [!DNL Platform Server]，例如Dynamic Media查看器( [!DNL /is-viewers/*])、静态流量和静态内容请求(由 [!DNL Platform Server] (例如， [!DNL /is-docs/*])。

请求 [!DNL /is-catalog] 和 [!DNL /is/cache] 根路径应始终从任何客户端流量分析中排除。
