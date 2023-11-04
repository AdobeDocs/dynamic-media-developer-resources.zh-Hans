---
description: 使用这些服务器设置来配置服务器。
solution: Experience Manager
title: 服务器
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# 服务器{#server}

使用这些服务器设置来配置服务器。

## SV：：ImageServerMode — 图像服务器模式 {#section-991b287f2dde4f77a24fc69d5b32cabd}

图像服务器的32位和64位版本均适用于Linux。 在64位Linux服务器上安装时指定ImageServer64，或在32位服务器上安装时指定ImageServer32（默认）。

>[!NOTE]
>
>图像服务器的64位版本不支持FlashPix源文件。

>[!NOTE]
>
>Windows不支持64位模式。 仅 `ImageServer32` 可以指定。 否则，图像服务不会启动。

## SV：：PsHeapSize - [!DNL Platform Server] 栈大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

的Java栈大小 [!DNL Platform Server]. 默认为&quot; `512m`“(512 MB)。

## IS：：TcpPort， PS：：isConnection.port — 图像服务器侦听端口 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用于在 [!DNL Platform Server] 和图像服务器。 请确保指定一个端口号，否则该端口不会用于主机系统。

>[!NOTE]
>
>要使图像服务正常工作，必须为设置相同的值 `IS::TcpPort` 和 `PS::isConnection.port`.

## IS：：PhysicalMemory — 映像服务器内存限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

内存中图像数据的近似限制，以物理内存的百分比表示。 有效范围为10%到90%。 如果可能，图像服务器会尝试将其对图像内存的使用限制为指定的数量。 在进行大量处理活动期间，可能会临时超出限制。

## IS：：WorkerThreads — 图像服务器工作线程Threads的数量 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

图像服务器用于处理图像数据的线程的最大数目。 默认值为0，这允许图像服务器自动优化线程计数。

某些操作系统具有线程模型，并且上下文交换开销很高。 在这种情况下，当选择特定线程计数（例如，每个CPU一个线程）时，整体服务器性能可能会提高。 可能需要进行一些试验才能找到最佳设置。 有关更多信息，请参阅图像服务发行说明和操作系统文档。

## IS：：NumberOfTextServers — 文本服务器实例数 {#section-971e20a90c1a473598fba738ed95671a}

同时处于活动状态的最大文本渲染器数量。 0（默认值）相当于可用CPU核心数的1.5倍。

## IS：：TextServerTcpPortRange — 文本服务器通信端口 {#section-a13465de88ed4df09931e5ba840c1942}

用于文本服务器通信的端口。 指定第一个和最后一个端口号，以“ — ”分隔。
