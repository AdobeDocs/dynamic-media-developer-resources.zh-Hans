---
description: 通过在嵌套/嵌入请求中指定cache=on，可以缓存由嵌套/嵌入图像提供和图像呈现请求生成的中间图像数据。 此数据以专有格式存储在响应数据缓存中。
solution: Experience Manager
title: 辅助数据缓存
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 辅助数据缓存{#auxiliary-data-caches}

通过在嵌套/嵌入请求中指定cache=on，可以缓存由嵌套/嵌入图像提供和图像呈现请求生成的中间图像数据。 此数据以专有格式存储在响应数据缓存中。

从外部HTTP服务器获得的图像也存储在响应数据缓存中。 在生成缓存条目之前，使用验证实用程序自动验证这些图像。

Platform Server可编译图像目录数据以进行有效访问。 此数据存储在`CS::CatalogCacheFolder`中。
