---
description: 使用这些服务器设置配置服务器。
seo-description: 使用这些服务器设置配置服务器。
seo-title: 服务器
solution: Experience Manager
title: 服务器
uuid: 50db98cc-8354-4884-9416-00808828061b
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# 服务器{#server}

使用这些服务器设置配置服务器。

## SV::ImageServerMode — 图像服务器模式{#section-991b287f2dde4f77a24fc69d5b32cabd}

图像服务器的32位和64位版本都可用于Linux。 如果安装在64位Linux服务器上，请指定ImageServer64；如果安装在32位服务器上，则指定ImageServer32（默认）。

>[!NOTE]
>
>64位版本的图像服务器不支持FlashPix源文件。

>[!NOTE]
>
>Windows不支持64位模式。 只能指定`ImageServer32`。 否则，图像服务将不开始。

## SV::PsHeapSize — 平台服务器堆大小{#section-fd83715948764aeda58d6b3a9f9f8be9}

平台服务器的Java堆大小。 默认为“ `512m`”(512 MB)。

## IS::TcpPort， PS::isConnection.port - Image Server侦听端口{#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用于平台服务器和图像服务器之间通信的端口。 请确保指定主机系统中未使用的端口号。

>[!NOTE]
>
>要使图像服务正常工作，必须为`IS::TcpPort`和`PS::isConnection.port`设置相同的值。

## IS::PhysicalMemory — 映像服务器内存限制{#section-85e37aa2ac6e456eb698da716dd3247d}

内存中图像数据的近似限制，以物理内存的百分比表示。 有效范围是10%到90%。 如果可能，图像服务器会尝试将图像内存的使用限制在指定数量。 在高处理活动，可以暂时超过该限制。

## IS::WorkerThreads — 映像服务器工作线程数{#section-e2946063b13c4f728cdf5dba3d8b4de1}

图像服务器用于处理图像数据的最大线程数。 默认值为0，这允许图像服务器自动优化线程计数。

某些操作系统具有线程模型，上下文切换开销较高。 在这种情况下，当选择特定线程计数（例如每CPU一个线程）时，整体服务器性能可以提高。 可能需要进行一些试验才能找到最佳设置。 有关更多信息，请参阅图像服务发行说明和操作系统文档。

## IS::NumberOfTextServers — 文本服务器实例数{#section-971e20a90c1a473598fba738ed95671a}

要同时处于活动状态的文本呈示器的最大数量。 0（默认）等于1.5倍的可用CPU核心数。

## IS::TextServerTcpPortRange — 文本服务器通信端口{#section-a13465de88ed4df09931e5ba840c1942}

用于文本服务器通信的端口。 指定第一个和最后一个端口号，以“ — ”分隔。
