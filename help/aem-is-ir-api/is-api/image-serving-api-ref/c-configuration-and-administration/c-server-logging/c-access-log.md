---
description: 这是主日志，用于跟踪对 [!DNL Platform Server]发出的所有HTTP请求。 图像渲染（如果启用）将其访问日志数据写入同一文件。
solution: Experience Manager
title: 访问日志
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# 访问日志{#access-log}

这是主日志，用于跟踪对[!DNL Platform Server]发出的所有HTTP请求。 图像渲染（如果启用）将其访问日志数据写入同一文件。

在server.xml中配置访问日志。

>[!NOTE]
>
>除了图像服务([!DNL /is/image/*])和图像渲染([!DNL /ir/render/*])的客户端流量之外，访问日志可能还包含某些内部流量：对[!DNL Platform Server]目录系统([!DNL /is-catalog/*])的访问、缓存共享和错误重定向请求([!DNL /is/cache/*])、对部署到[!DNL Platform Server]的其他包的访问(例如Dynamic Media查看器([!DNL /is-viewers/*])、由[!DNL Platform Server]服务的静态流量和静态内容请求（例如[!DNL /is-docs/*]）。

应始终从任何客户端流量分析中排除具有[!DNL /is-catalog]和[!DNL /is/cache]根路径的请求。
