---
description: “图像渲染”使用的内存量可能差异很大，并且高度取决于实际服务器负载和使用情况（例如，很少使用晕影，与许多不同的晕影、晕影的大小和复杂性等）。
solution: Experience Manager
title: 内存注意事项
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# 内存注意事项{#memory-considerations}

“图像渲染”使用的内存量可能差异很大，并且高度取决于实际服务器负载和使用情况（例如，很少使用晕影，与许多不同的晕影、晕影的大小和复杂性等）。

为获得最佳性能，应避免内存分页（交换）。

图像渲染共享图像服务器的内存管理。 使用“图像渲染”时，应分配额外的内存。 30%到50%的物理内存可能是合理的。

有关如何更改图像服务器内存分配(ImageServer::PhysicalMemory)的信息，请参阅图像服务文档。
