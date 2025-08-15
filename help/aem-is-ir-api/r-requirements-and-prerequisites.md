---
title: 系统要求和先决条件
description: 在使用Dynamic Media图像服务之前，请确保您的系统符合系统要求。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# 系统要求和先决条件{#system-requirements-and-prerequisites}

在使用Dynamic Media图像服务之前，请确保您的系统符合系统要求。

## 服务器硬件 {#section-f3c14a7bc1b745118602659628df779f}

您的服务器应满足以下硬件要求。

>[!NOTE]
>
>处理器采用AMD64和英特尔® EM64T的系统通常配置为NUMA（非统一内存体系结构）平台。 这意味着内核在启动时构建多个内存节点，而不是构建单个内存节点。 该多节点结构可导致一个或多个节点上的存储器耗尽，而其它节点则被耗尽。 当内存耗尽时，即使存在可用内存，内核也可以决定终止进程（例如，图像服务器或[!DNL Platform Server]）。 因此，Adobe建议，如果运行此类系统，请关闭NUMA。 使用`numa=off`启动选项可避免内核停止这些进程。

**Windows**

* 英特尔至强®或AMD®皓龙CPU，至少具有四个内核。
* 最少1 GB RAM。
* 交换空间至少相当于物理内存(RAM)容量的两倍。
* 2 GB的可用硬盘空间用于安装和基本操作，但源映像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网卡。

**Linux®**

* 英特尔至强®或AMD®皓龙CPU，至少具有四个内核。
* 最少16 GB RAM。
* 已禁用交换（推荐）。
* 2 GB的可用硬盘空间用于安装和基本操作，但源映像、日志、数据缓存和清单文件需要额外的磁盘空间。
* 快速以太网网卡。

**注意(Linux®)：**&#x200B;打开SELinux时，图像服务不起作用。 此选项默认处于启用状态。 要禁用SELinux，请编辑[!DNL /etc/selinux/config]文件并将SELinux值从以下位置更改：

`SELINUX=enforcing`

收件人

`SELINUX=disabled`

**注意(Linux®)：**&#x200B;请确保服务器的主机名可解析为IP地址。 如果无法执行此操作，请将完全限定的主机名和IP地址添加到[!DNL /etc/hosts]，如下例所示。

`<ip address> <fully qualified hostname>`

## 服务器软件 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media图像服务需要以下服务器软件。

**Windows**

* Microsoft® Windows Server 2008。
* 64位操作系统

**Linux®**

* Red Hat® Enterprise 5或CentOS 5.5及更高版本，带有最新的修补程序包。
* 64位操作系统

**注意：**&#x200B;要在Windows上使用图像服务，必须安装Microsoft® Visual Studio 2010。
