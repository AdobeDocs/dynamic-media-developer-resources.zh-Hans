---
title: 响应数据缓存
description: ' [!DNL Platform Server] 将所有回复图像和特定文本数据缓存到磁盘，除非请求标记为不可缓存。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 响应数据缓存{#response-data-cache}

[!DNL Platform Server]将所有回复图像和某些文本数据缓存到磁盘，除非请求标记为不可缓存。

[!DNL Platform Server]的磁盘缓存的位置设置为`PS::cache.rootPaths`。

对于具有高缓存命中率的应用程序，可以通过在多个磁盘设备之间分发响应数据缓存来提高服务器性能和容量。 您通过在每个磁盘上创建缓存根文件夹并在`PS::cache.rootPaths`中注册它们来实现此操作。

`PS::cache.maxSize`指定所有缓存项的总大小，不考虑任何文件系统开销。 所需的磁盘空间量取决于文件系统属性（如磁盘块大小）和缓存条目数。 为HTTP磁盘缓存预留的磁盘空间是`PS::cache.maxSize`所指定数量的两倍。 使用最近最少使用的算法来使缓存的数据量保持在限制之内。

除了`PS::cache.maxSize`之外，响应缓存也通过限制包含`PS::cache.maxEntries`的缓存项的最大数量来管理。 在Linux®上，此设置指定的值不能大于缓存分区上可用的inode数。

>[!NOTE]
>
>[!DNL Platform Server]维护内存中缓存索引。 此索引的大小是`PS::cache.maxEntries`值的32字节倍。 如有必要，请增加[!DNL Platform Server]栈大小以容纳更大的缓存。

当服务器按顺序关闭时，系统将使用保存到磁盘的高速缓存索引文件。 如果发生意外事件（如电源故障），则可能无法保存此文件。 此外，[!DNL Platform Server]可能需要几分钟才能准备就绪。
