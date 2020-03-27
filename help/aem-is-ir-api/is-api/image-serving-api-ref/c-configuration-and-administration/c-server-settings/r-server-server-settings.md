---
description: 使用这些服务器设置配置服务器。
seo-description: 使用这些服务器设置配置服务器。
seo-title: 服务器
solution: Experience Manager
title: 服务器
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 服务器{#server}

使用这些服务器设置配置服务器。

## SV::ImageServerMode —— 图像服务器模式 {#section-991b287f2dde4f77a24fc69d5b32cabd}

32位和64位版本的图像服务器都可用于Linux。 如果安装在64位Linux服务器上，请指定ImageServer64；如果安装在32位服务器上，请指定ImageServer32（默认）。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>图像服务器的64位版本不支持FlashPix源文件。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Windows不支持64位模式。 只能 `ImageServer32` 指定。 否则，图像服务将不开始。

## SV::PsHeapSize —— 平台服务器堆大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

平台服务器的Java堆大小。 默认为“ `512m`”(512 MB)。

## IS::TcpPort, PS::isConnection.port —— 图像服务器监听端口 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用于平台服务器和图像服务器之间通信的端口。 请务必指定主机系统中未使用的端口号。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>要使图像服务正常工作，必须为和设置相同 `IS::TcpPort` 的值 `PS::isConnection.port`。

## IS::PhysicalMemory —— 图像服务器内存限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

内存中图像数据的近似限制，以物理内存的百分比表示。 有效范围为10%到90%。 图像服务器尝试将图像内存的使用限制在指定的数量（如果可能）。 在重处理活动期间，可以临时超出该限制。

## IS::WorkerThreads —— 图像服务器工作线程数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

图像服务器用于处理图像数据的最大线程数。 默认值为0，这允许图像服务器自动优化线程数。

某些操作系统的线程模型具有高上下文切换开销。 在这种情况下，当选择特定线程计数时（例如每CPU一个线程），整体服务器性能可以提高。 可能需要进行一些试验才能找到最佳设置。 有关更多信息，请参阅图像服务发行说明和操作系统文档。

## IS::NumberOfTextServers —— 文本服务器实例数 {#section-971e20a90c1a473598fba738ed95671a}

同时处于活动状态的文本渲染器的最大数量。 0（默认）等于1.5倍的可用CPU核心数。

## IS::TextServerTcpPortRange —— 文本服务器通信端口 {#section-a13465de88ed4df09931e5ba840c1942}

用于文本服务器通信的端口。 指定第一个和最后一个端口号，以“-”分隔。
