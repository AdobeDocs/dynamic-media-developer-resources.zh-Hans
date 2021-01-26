---
description: 平台服务器将所有回复图像和特定文本数据缓存到磁盘，除非将请求标记为不可缓存。
seo-description: 平台服务器将所有回复图像和特定文本数据缓存到磁盘，除非将请求标记为不可缓存。
seo-title: 响应数据缓存
solution: Experience Manager
title: 响应数据缓存
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# 响应数据缓存{#response-data-cache}

平台服务器将所有回复图像和特定文本数据缓存到磁盘，除非将请求标记为不可缓存。

平台服务器的磁盘缓存的位置设置为`PS::cache.rootPaths`。

对于高速缓存命中率较高的应用程序，可以通过在多个磁盘设备之间分发响应数据高速缓存来提高服务器性能和容量。 要完成此操作，请在每个磁盘上创建一个缓存根文件夹，然后在`PS::cache.rootPaths`中注册。

`PS::cache.maxSize` 指定所有缓存条目的总大小，不考虑任何文件系统开销。实际需要的磁盘空间量取决于文件系统属性（如磁盘块大小）和缓存条目数。 建议为HTTP磁盘缓存保留的磁盘空间是`PS::cache.maxSize`指定的磁盘空间量的两倍。 使用最少最近使用的算法来将高速缓存的数据量保持在限制内。

除了`PS::cache.maxSize`之外，还通过限制具有`PS::cache.maxEntries`的最大缓存条目数来管理响应缓存。 在Linux上，此设置必须指定一个不大于缓存分区上可用节点数的值。

>[!NOTE]
>
>平台服务器维护内存中的缓存索引。 此索引的大小是`PS::cache.maxEntries`值的32字节倍。 您可能需要增加平台服务器堆大小以适应较大的缓存。

系统使用缓存索引文件，当服务器按顺序关闭时保存到磁盘。 如果出现意外事件（如电源故障），则可能无法保存此文件。 此外，平台服务器可能需要几分钟才能准备就绪。
