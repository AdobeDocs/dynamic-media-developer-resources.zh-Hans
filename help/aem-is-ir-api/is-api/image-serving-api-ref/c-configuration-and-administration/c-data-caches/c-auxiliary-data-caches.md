---
description: 通过在嵌套/嵌入的请求中指定cache=on，可以缓存由嵌套/嵌入的图像服务和图像渲染请求生成的中间图像数据。 此数据以专有格式存储在响应数据缓存中。
solution: Experience Manager
title: 辅助数据缓存
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# 辅助数据缓存{#auxiliary-data-caches}

通过在嵌套/嵌入的请求中指定cache=on，可以缓存由嵌套/嵌入的图像服务和图像渲染请求生成的中间图像数据。 此数据以专有格式存储在响应数据缓存中。

从外部HTTP服务器获得的图像也存储在响应数据缓存中。 在生成缓存条目之前，使用验证实用程序自动验证这些图像。

平台服务器编译图像目录数据，以便有效访问。 此数据存储在`CS::CatalogCacheFolder`中。
