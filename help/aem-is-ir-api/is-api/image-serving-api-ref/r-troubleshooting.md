---
description: 本部分包含对图像服务偶尔出现问题的解决方案。
solution: Experience Manager
title: 疑难解答
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 疑难解答{#troubleshooting}

本部分包含对图像服务偶尔出现问题的解决方案。

**常规**

ImageServer现在保留升级安装期间更改的所有文件的安装日志和备份文件夹。 此文件和文件夹可能位于图像服务安装目录的根目录下。

**启动图像服务器时，启动脚本将停止，并显示消息“start pending”（仅适用于LINUX）**

这可能表示图像服务许可证存在问题，例如缺少许可证文件或临时许可证已过期。 有效的许可证文件必须位于 [!DNL /usr/local/scene7/licenses].

**图像服务器停止或崩溃，并且图像服务器日志文件指示没有足够的空间或“资源在文件中暂时不可用” [!DNL IgcVirtualMemory.cpp]&quot;**

此错误消息的原因是图像服务器未能分配其配置为使用的内存量。

* 检查中的物理内存设置 [!DNL ImageServerRegistry.xml]. 如果其他内存密集型应用程序在同一系统上运行，则不应超过50%。 默认值为20%。
* 确保服务器上的交换空间至少是物理RAM大小的两倍。 交换空间设置不足可能导致此问题。

**缓存文件夹使用的实际磁盘空间超过 ` *[!DNL cache.maxSize]*`在中设置[!DNL PlatformServer.conf]**

这并不表示有问题。 文件系统开销不包括在中 [!DNL Platform Server]的磁盘缓存设置。 所述系统报告的总量可以显着高于所述设置。 建议保留两倍的磁盘空间 ` *[!DNL cache.maxSize]*`.

**is-docs示例中的图像损坏**

如果映像服务器未运行，则会发生这种情况。 如果目录根路径或映像根路径已从安装默认路径更改为其他路径，但示例映像和目录尚未移动到新位置，也会发生这种情况。 检查配置文件中的“映像服务器根路径”值。 如有必要，请将包含示例图像的演示文件夹移动到当前图像根目录，然后移动 [!DNL sample*.*] 到当前目录根目录。

这些示例还假定中的某些设置 [!DNL default.ini] 是标准的（例如，不得启用模糊处理或锁定）。

**长时间正常运行后出现过多缓存未命中**

根据服务器使用情况，可以通过提高服务器性能来提高性能 [!DNL Platform Server] 如果磁盘空间可用，则为磁盘缓存大小。 可以通过手动编辑配置文件来更改设置。 请参阅文档。

**日志文件占用太多磁盘空间**

图像服务器和 [!DNL Platform Server] 每天启动一个新日志文件。 默认情况下，这些目录将放在[！DNL *[!DNL install_root]*/ImageServing/logs]。 日志文件大小、保留的日志数以及可以配置的日志内容。 请参阅文档。

**如果您的服务器上安装了防病毒软件**

建议您关闭图像服务目录的扫描。 否则，扫描大容量读/写目录（如缓存、图像、字体、配置文件和目录目录）可能会导致问题。

**Digimarc导致缩放图像的性能问题**

请勿在缩放的图像上使用Digimarc。 性能不可接受。 如有必要，请为要用于缩放的图像创建单独的目录，并禁用该目录的Digimarc。
