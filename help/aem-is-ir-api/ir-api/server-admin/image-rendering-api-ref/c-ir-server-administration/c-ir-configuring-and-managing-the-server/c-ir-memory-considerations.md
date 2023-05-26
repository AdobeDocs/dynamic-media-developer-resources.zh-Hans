---
description: 图像渲染使用的内存量差别很大，并且很大程度上取决于实际的服务器负载和使用情况（例如，只有少数几个晕影，而许多不同的晕影、晕影的大小和复杂性等等）。
solution: Experience Manager
title: 内存注意事项
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# 内存注意事项{#memory-considerations}

图像渲染使用的内存量差别很大，并且很大程度上取决于实际的服务器负载和使用情况（例如，只有少数几个晕影，而许多不同的晕影、晕影的大小和复杂性等等）。

为获得最佳性能，应避免内存分页（交换）。

图像渲染共享图像服务器的内存管理。 使用图像渲染时，应分配额外的内存。 30%到50%的物理内存可能是合理的。

有关如何更改图像服务器内存分配(ImageServer：：PhysicalMemory)的信息，请参阅图像服务文档。
