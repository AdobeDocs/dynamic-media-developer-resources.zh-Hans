---
description: 使用这些服务器设置来配置服务器。
solution: Experience Manager
title: 服务器
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
TQID: 'https://experienceleague.adobe.com/403CInOL4425Gv35Njb69WSo-QRyvTuDUZEBtNRsvj0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 357
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
>Windows不支持64位模式。 只能指定`ImageServer32`。 否则，图像服务不会启动。

## SV：：PsHeapSize - [!DNL Platform Server]栈大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

[!DNL Platform Server]的Java栈大小。 默认为“`512m`”(512 MB)。

## IS：：TcpPort， PS：：isConnection.port — 图像服务器侦听端口 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用于[!DNL Platform Server]和图像服务器之间通信的端口。 请确保指定一个端口号，否则该端口不会用于主机系统。

>[!NOTE]
>
>要使图像服务正常工作，必须为`IS::TcpPort`和`PS::isConnection.port`设置相同的值。

## IS：：PhysicalMemory — 映像服务器内存限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

内存中图像数据的近似限制，以物理内存的百分比表示。 有效范围为10%到90%。 如果可能，图像服务器会尝试将其对图像内存的使用限制为指定的数量。 在进行大量处理活动期间，可能会临时超出限制。

## IS：：WorkerThreads — 图像服务器工作线程Threads的数量 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

图像服务器用于处理图像数据的线程的最大数目。 默认值为0，这允许图像服务器自动优化线程计数。

某些操作系统具有线程模型，并且上下文交换开销很高。 在这种情况下，当选择特定线程计数（例如，每个CPU一个线程）时，整体服务器性能可能会提高。 可能需要进行一些试验才能找到最佳设置。 有关更多信息，请参阅图像服务发行说明和操作系统文档。

## IS：：NumberOfTextServers — 文本服务器实例数 {#section-971e20a90c1a473598fba738ed95671a}

同时处于活动状态的最大文本渲染器数量。 0（默认）相当于可用CPU核心数量的1.5倍。

## IS：：TextServerTcpPortRange — 文本服务器通信端口 {#section-a13465de88ed4df09931e5ba840c1942}

用于文本服务器通信的端口。 指定第一个和最后一个端口号，以“ — ”分隔。
