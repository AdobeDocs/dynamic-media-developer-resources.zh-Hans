---
description: 图像渲染使用的内存量可能差异很大，并且高度取决于实际的服务器负载和使用情况（例如，与许多不同的晕影相比，很少，晕影的大小和复杂性等）。
seo-description: 图像渲染使用的内存量可能差异很大，并且高度取决于实际的服务器负载和使用情况（例如，与许多不同的晕影相比，很少，晕影的大小和复杂性等）。
seo-title: 内存注意事项
solution: Experience Manager
title: 内存注意事项
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# 内存注意事项{#memory-considerations}

图像渲染使用的内存量可能差异很大，并且高度取决于实际的服务器负载和使用情况（例如，与许多不同的晕影相比，很少，晕影的大小和复杂性等）。

为获得最佳性能，应避免内存分页（交换）。

图像渲染共享图像服务器的内存管理。 使用图像渲染时，应分配额外的内存。 30%到50%的物理内存可能是合理的。

有关如何更改图像服务器内存分配(ImageServer::PhysicalMemory)的信息，请参阅图像服务文档。
