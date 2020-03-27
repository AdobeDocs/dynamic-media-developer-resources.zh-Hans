---
description: 在使用Scene7图像服务之前，请确保您的系统满足系统要求。
seo-description: 在使用Scene7图像服务之前，请确保您的系统满足系统要求。
seo-title: 系统要求和先决条件
solution: Experience Manager
title: 系统要求和先决条件
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 系统要求和先决条件{#system-requirements-and-prerequisites}

在使用Scene7图像服务之前，请确保您的系统满足系统要求。

## 服务器硬件 {#section-f3c14a7bc1b745118602659628df779f}

您的服务器应满足以下硬件要求。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>具有AMD64和Intel® EM64T处理器的系统通常配置为NUMA（非统一内存架构）平台。 这意味着内核在启动时构造多个存储器节点，而不是构造单个存储器节点。 该多节点构造可导致在其它节点耗尽之前，一个或多个节点上的存储器耗尽。 当内存耗尽时，内核可决定终止进程（例如，图像服务器或平台服务器），即使有可用内存。 因此，Adobe Systems建议，如果您运行这样的系统，则关闭NUMA。 使用 `numa=off` 开始选项可避免内核停止这些进程。

**Windows**

* Intel Xeon®或AMD® Opteron CPU至少具有4个核。
* 最低16GB内存。
* 交换空间至少等于物理内存(RAM)量的两倍。
* 2 GB可用硬盘空间用于安装和基本操作，源图像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网络接口卡。

**Linux**

* Intel Xeon®或AMD® Opteron CPU至少具有4个核。
* 最低16GB内存。
* 已禁用交换（建议）。
* 2 GB可用硬盘空间用于安装和基本操作，源图像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网络接口卡。

**注意(Linux):** 打开SELinux时，图像服务不工作。 此选项默认处于启用状态。 要禁用SELinux，请编辑文 [!DNL /etc/selinux/config] 件并将SELinux值从：

`SELINUX=enforcing`

至

`SELINUX=disabled`

**注意(Linux):** 确保服务器的主机名可解析为IP地址。 如果这不可能，请将完全限定的主机名和IP地址添加 [!DNL /etc/hosts] 到，如下例所示。

`<ip address> <fully qualified hostname>`

## 服务器软件 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Scene7图像服务需要以下服务器软件。

**Windows**

* Microsoft® Windows 2008 Server。
* 64位操作系统。

**Linux**

* Red Hat® Enterprise 5或CentOS 5.5及更高版本以及最新的修补程序。
* 64位操作系统。

**注意：** 要在Windows上使用图像服务，必须安装Microsoft Visual Studio 2010可再分发版。 可在以下位置进行再分发：

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

