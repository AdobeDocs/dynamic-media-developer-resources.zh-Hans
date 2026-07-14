---
description: 图像渲染使用的内存量可能会大不相同，并且很大程度上取决于实际的服务器负载和使用情况（例如，很少有与许多不同的晕影、晕影的大小和复杂性等）。
solution: Experience Manager
title: 内存注意事项
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
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
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# 内存注意事项{#memory-considerations}

图像渲染使用的内存量可能会大不相同，并且很大程度上取决于实际的服务器负载和使用情况（例如，很少有与许多不同的晕影、晕影的大小和复杂性等）。

为获得最佳性能，应避免内存分页（交换）。

图像渲染共享图像服务器的内存管理。 使用图像渲染时，应分配额外的内存。 30%到50%的物理内存可能是合理的。

有关如何更改图像服务器内存分配(ImageServer：：PhysicalMemory)的信息，请参阅图像服务文档。

