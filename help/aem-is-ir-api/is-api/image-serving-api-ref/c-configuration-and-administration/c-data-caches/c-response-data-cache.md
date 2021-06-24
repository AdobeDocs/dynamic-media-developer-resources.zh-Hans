---
description: Platform Server将所有回复图像和某些文本数据缓存到磁盘，除非将请求标记为不可缓存。
solution: Experience Manager
title: 响应数据缓存
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 响应数据缓存{#response-data-cache}

Platform Server将所有回复图像和某些文本数据缓存到磁盘，除非将请求标记为不可缓存。

Platform Server的磁盘缓存的位置通过`PS::cache.rootPaths`进行设置。

对于缓存命中率较高的应用程序，您可以通过在多个磁盘设备之间分配响应数据缓存来提高服务器性能和容量。 要完成此操作，请在每个磁盘上创建一个缓存根文件夹，并在`PS::cache.rootPaths`中注册。

`PS::cache.maxSize` 指定所有缓存条目的总大小，而不考虑任何文件系统开销。实际需要的磁盘空间量取决于文件系统属性（如磁盘块大小）和缓存条目数。 建议为HTTP磁盘缓存保留的磁盘空间是`PS::cache.maxSize`指定的磁盘空间量的两倍。 使用最近使用的算法将缓存数据量保持在限制内。

除了`PS::cache.maxSize`之外，还通过限制具有`PS::cache.maxEntries`的最大缓存条目数来管理响应缓存。 在Linux上，此设置必须指定一个值，该值必须不大于缓存分区上可用inode的数量。

>[!NOTE]
>
>平台服务器维护内存中的缓存索引。 此索引的大小是`PS::cache.maxEntries`值的32字节。 您可能需要增加Platform Server堆大小以容纳较大的缓存。

系统使用缓存索引文件，当服务器按顺序关闭时，该文件会保存到磁盘中。 如果发生电源故障等意外事件，可能无法保存此文件。 此外，平台服务器可能需要几分钟才能准备就绪。
