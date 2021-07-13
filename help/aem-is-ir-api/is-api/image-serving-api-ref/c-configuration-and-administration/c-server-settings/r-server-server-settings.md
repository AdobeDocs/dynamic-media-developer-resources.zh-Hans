---
description: 使用这些服务器设置来配置您的服务器。
solution: Experience Manager
title: 服务器
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 服务器{#server}

使用这些服务器设置来配置您的服务器。

## SV::ImageServerMode — 图像服务器模式 {#section-991b287f2dde4f77a24fc69d5b32cabd}

32位和64位版本的图像服务器都适用于Linux。 如果安装在64位Linux服务器上，请指定ImageServer64；如果安装在32位服务器上，请指定ImageServer32（默认）。

>[!NOTE]
>
>图像服务器的64位版本不支持FlashPix源文件。

>[!NOTE]
>
>Windows不支持64位模式。 只能指定`ImageServer32`。 否则，将不会启动图像提供。

## SV::PsHeapSize — 平台服务器堆大小 {#section-fd83715948764aeda58d6b3a9f9f8be9}

平台服务器的Java堆大小。 默认为“ `512m`”(512 MB)。

## IS::TcpPort， PS::isConnection.port — 图像服务器侦听端口 {#section-5421bfd2ca2a4a979faf812b6fdb2887}

指定用于平台服务器与图像服务器之间通信的端口。 确保指定主机系统上未使用的端口号。

>[!NOTE]
>
>为了使图像服务正常工作，必须为`IS::TcpPort`和`PS::isConnection.port`设置相同的值。

## IS::PhysicalMemory — 图像服务器内存限制 {#section-85e37aa2ac6e456eb698da716dd3247d}

内存中图像数据的近似限制，以物理内存的百分比表示。 有效范围为10%到90%。 图像服务器尝试将其对图像内存的使用限制为指定的数量（如果可能）。 在繁重的处理活动期间，可能会暂时超出限制。

## IS::WorkerThreads — 图像服务器工作线程数 {#section-e2946063b13c4f728cdf5dba3d8b4de1}

图像服务器用于处理图像数据的最大线程数。 默认值为0，这允许图像服务器自动优化线程数。

某些操作系统具有线程模型，且上下文切换开销较高。 在这种情况下，当选择特定线程计数（例如每个CPU一个线程）时，整体服务器性能可能会提高。 可能需要进行一些实验以找到最佳设置。 有关其他信息，请参阅图像提供发行说明和操作系统文档。

## IS::NumberOfTextServers — 文本服务器实例数 {#section-971e20a90c1a473598fba738ed95671a}

同时处于活动状态的文本渲染器的最大数量。 0（默认）等于可用CPU核心数的1.5倍。

## IS::TextServerTcpPortRange — 文本服务器通信端口 {#section-a13465de88ed4df09931e5ba840c1942}

用于文本服务器通信的端口。 指定第一个和最后一个端口号（以“ — ”分隔）。
