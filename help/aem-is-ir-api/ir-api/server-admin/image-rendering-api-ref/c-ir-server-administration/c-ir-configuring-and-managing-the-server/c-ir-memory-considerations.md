---
description: “图像渲染”使用的内存量可能会有很大差异，并且这在很大程度上取决于实际的服务器负载和使用情况（例如，与许多不同的晕影相比，很少有的晕影、晕影的大小和复杂性等）。
solution: Experience Manager
title: 内存注意事项
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 内存注意事项{#memory-considerations}

“图像渲染”使用的内存量可能会有很大差异，并且这在很大程度上取决于实际的服务器负载和使用情况（例如，与许多不同的晕影相比，很少有的晕影、晕影的大小和复杂性等）。

为获得最佳性能，应避免内存分页（交换）。

图像渲染共享图像服务器的内存管理。 使用“图像渲染”时，应该分配额外的内存。 30%到50%的物理内存是合理的。

有关如何更改图像服务器内存分配(ImageServer::PhysicalMemory)的信息，请参阅图像服务文档。
