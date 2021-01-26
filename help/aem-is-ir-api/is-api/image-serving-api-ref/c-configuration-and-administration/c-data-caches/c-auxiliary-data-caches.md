---
description: 通过在嵌套／嵌入的请求中指定cache=on，可以缓存由嵌套／嵌入的图像服务和图像渲染请求生成的中间图像数据。 此数据以专有格式存储在响应数据缓存中。
seo-description: 通过在嵌套／嵌入的请求中指定cache=on，可以缓存由嵌套／嵌入的图像服务和图像渲染请求生成的中间图像数据。 此数据以专有格式存储在响应数据缓存中。
seo-title: 辅助数据缓存
solution: Experience Manager
title: 辅助数据缓存
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# 辅助数据缓存{#auxiliary-data-caches}

通过在嵌套／嵌入的请求中指定cache=on，可以缓存由嵌套／嵌入的图像服务和图像渲染请求生成的中间图像数据。 此数据以专有格式存储在响应数据缓存中。

从外部HTTP服务器获得的图像也存储在响应数据缓存中。 在生成缓存条目之前，使用验证实用程序自动验证这些图像。

平台服务器编译图像目录数据，以便有效访问。 此数据存储在`CS::CatalogCacheFolder`中。
