---
description: 这是主日志，用于跟踪向发出的所有HTTP请求 [!DNL Platform Server]. 图像渲染（如果启用）将其访问日志数据写入同一文件。
solution: Experience Manager
title: 访问日志
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 访问日志{#access-log}

这是主日志，用于跟踪向发出的所有HTTP请求 [!DNL Platform Server]. 图像渲染（如果启用）将其访问日志数据写入同一文件。

在server.xml中配置访问日志。

>[!NOTE]
>
>除了图像服务的客户端流量之外( [!DNL /is/image/*])和图像渲染( [!DNL /ir/render/*])，则访问日志可能包括某些内部流量：访问 [!DNL Platform Server] 目录系统( [!DNL /is-catalog/*])，缓存共享和错误重定向请求( [!DNL /is/cache/*])，访问部署到的其他包 [!DNL Platform Server]，例如Dynamic Media查看器( [!DNL /is-viewers/*])，由提供的静态流量和静态内容请求 [!DNL Platform Server] (例如， [!DNL /is-docs/*])。

请求 [!DNL /is-catalog] 和 [!DNL /is/cache] 根路径应始终从任何客户端流量分析中排除。
