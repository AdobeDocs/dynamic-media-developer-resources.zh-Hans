---
description: 在使用Dynamic Media图像服务之前，请确保您的系统满足系统要求。
solution: Experience Manager
title: 系统要求和先决条件
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 1%

---

# 系统要求和先决条件{#system-requirements-and-prerequisites}

在使用Dynamic Media图像服务之前，请确保您的系统满足系统要求。

## 服务器硬件 {#section-f3c14a7bc1b745118602659628df779f}

您的服务器应满足以下硬件要求。

>[!NOTE]
>
>具有AMD64和英特尔® EM64T处理器的系统通常配置为NUMA（非统一内存架构）平台。 这意味着内核在启动时构建多个内存节点，而不是构建单个内存节点。 该多节点构造可导致在其它节点耗尽之前一个或多个节点上的内存耗尽。 当内存耗尽时，内核可能会决定终止进程（例如，图像服务器或平台服务器），即使内存可用。 因此，Adobe Systems建议，如果您运行这样的系统，则关闭NUMA。 使用`numa=off`开始选项可避免内核停止这些进程。

**Windows**

* 至少具有4个内核的英特尔至强®或AMD®皓龙CPU。
* 最小16GB RAM。
* 交换空间至少等于物理内存(RAM)量的两倍。
* 2 GB的可用硬盘空间用于安装和基本操作，源映像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网卡。

**Linux**

* 至少具有4个内核的英特尔至强®或AMD®皓龙CPU。
* 最小16GB RAM。
* 交换已禁用（建议）。
* 2 GB的可用硬盘空间用于安装和基本操作，源映像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网卡。

**注意(Linux):** 打开SELinux时，图像提供不起作用。默认情况下，此选项处于启用状态。 要禁用SELinux，请编辑[!DNL /etc/selinux/config]文件，并将SELinux值从：

`SELINUX=enforcing`

至

`SELINUX=disabled`

**注意(Linux):** 确保服务器的主机名可解析为IP地址。如果无法实现，请将完全限定的主机名和IP地址添加到[!DNL /etc/hosts]中，如以下示例所示。

`<ip address> <fully qualified hostname>`

## 服务器软件 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving需要以下服务器软件。

**Windows**

* Microsoft® Windows 2008 Server。
* 64位操作系统。

**Linux**

* Red Hat® Enterprise 5或CentOS 5.5及更高版本，带有最新的修补程序。
* 64位操作系统。

**注意：** 要在Windows上使用图像服务，必须安装Microsoft Visual Studio 2010可再发行版。可再分发的地点如下：

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)
