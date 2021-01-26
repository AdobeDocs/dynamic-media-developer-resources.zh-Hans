---
description: 在使用Dynamic Media图像服务之前，请确保您的系统满足系统要求。
seo-description: 在使用Dynamic Media图像服务之前，请确保您的系统满足系统要求。
seo-title: 系统要求和先决条件
solution: Experience Manager
title: 系统要求和先决条件
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 1%

---


# 系统要求和先决条件{#system-requirements-and-prerequisites}

在使用Dynamic Media图像服务之前，请确保您的系统满足系统要求。

## 服务器硬件{#section-f3c14a7bc1b745118602659628df779f}

服务器应满足以下硬件要求。

>[!NOTE]
>
>具有AMD64和英特尔® EM64T处理器的系统通常配置为NUMA（非统一内存架构）平台。 这意味着内核在启动时构建多个内存节点，而不是构建单个内存节点。 该多节点构造可导致在其它节点耗尽之前，一个或多个节点上的内存耗尽。 当内存耗尽时，内核可决定终止进程（例如，映像服务器或平台服务器），即使内存可用。 因此，Adobe Systems建议，如果运行这样的系统，应关闭NUMA。 使用`numa=off`开始选项可避免内核停止这些进程。

**Windows**

* Intel Xeon®或AMD® Opteron CPU至少具有4个内核。
* 最低16GB内存。
* 交换空间至少等于物理内存(RAM)量的两倍。
* 2 GB可用硬盘空间用于安装和基本操作，源映像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网络接口卡。

**Linux**

* Intel Xeon®或AMD® Opteron CPU至少具有4个内核。
* 最低16GB内存。
* 交换已禁用（建议）。
* 2 GB可用硬盘空间用于安装和基本操作，源映像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网络接口卡。

**注意(Linux)：图** 像服务在打开SELinux时不工作。此选项默认处于启用状态。 要禁用SELinux，请编辑[!DNL /etc/selinux/config]文件，并将SELinux值从：

`SELINUX=enforcing`

至

`SELINUX=disabled`

**注意(Linux):** 确保服务器的主机名可解析为IP地址。如果这不可能，请按照以下示例将完全限定的主机名和IP地址添加到[!DNL /etc/hosts]。

`<ip address> <fully qualified hostname>`

## 服务器软件{#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media图像服务需要以下服务器软件。

**Windows**

* Microsoft® Windows 2008 Server。
* 64位操作系统。

**Linux**

* Red Hat® Enterprise 5或CentOS 5.5及更高版本以及最新的修补程序。
* 64位操作系统。

**注意：** 要在Windows上使用图像服务，必须安装Microsoft Visual Studio 2010可再分发版。可再发行产品可在以下位置使用：

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

