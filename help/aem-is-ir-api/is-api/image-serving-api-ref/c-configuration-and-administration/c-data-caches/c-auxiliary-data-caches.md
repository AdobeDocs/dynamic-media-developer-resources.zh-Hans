---
description: 通过在嵌套/嵌入请求中指定cache=on，可以缓存嵌套/嵌入图像服务和图像渲染请求生成的中间图像数据。 该数据以专有格式存储在响应数据缓存中。
solution: Experience Manager
title: 辅助数据缓存
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: 'https://experienceleague.adobe.com/oRZFSXKaBE9q7liBPRVCheL-NPTriPJkWZFqgMBcoaQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# 辅助数据缓存{#auxiliary-data-caches}

通过在嵌套/嵌入请求中指定cache=on，可以缓存嵌套/嵌入图像服务和图像渲染请求生成的中间图像数据。 该数据以专有格式存储在响应数据缓存中。

从外部HTTP服务器获得的图像也存储在响应数据缓存中。 在生成缓存条目之前，会使用验证实用程序自动验证此类图像。

[!DNL Platform Server]编译图像目录数据以便有效访问。 此数据存储在`CS::CatalogCacheFolder`中。
