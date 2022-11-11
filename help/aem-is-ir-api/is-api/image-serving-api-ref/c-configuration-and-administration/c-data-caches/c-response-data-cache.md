---
description: 的 [!DNL Platform Server] 将所有回复图像和某些文本数据缓存到磁盘，除非将请求标记为不可缓存。
solution: Experience Manager
title: 响应数据缓存
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 响应数据缓存{#response-data-cache}

的 [!DNL Platform Server] 将所有回复图像和某些文本数据缓存到磁盘，除非将请求标记为不可缓存。

的位置 [!DNL Platform Server]的磁盘缓存设置为 `PS::cache.rootPaths`.

对于缓存命中率较高的应用程序，您可以通过在多个磁盘设备之间分配响应数据缓存来提高服务器性能和容量。 为此，请在每个磁盘上创建一个缓存根文件夹，并在中注册 `PS::cache.rootPaths`.

`PS::cache.maxSize` 指定所有缓存条目的总大小，而不考虑任何文件系统开销。 实际需要的磁盘空间量取决于文件系统属性（如磁盘块大小）和缓存条目数。 建议为HTTP磁盘缓存保留的磁盘空间是指定的磁盘空间量的两倍 `PS::cache.maxSize`. 使用最近使用的算法将缓存数据量保持在限制内。

除 `PS::cache.maxSize`，则响应缓存也可通过限制 `PS::cache.maxEntries`. 在Linux上，此设置必须指定一个值，该值必须不大于缓存分区上可用inode的数量。

>[!NOTE]
>
>的 [!DNL Platform Server] 维护内存中的缓存索引。 此索引的大小是 `PS::cache.maxEntries`. 您可能需要将 [!DNL Platform Server] 堆大小以容纳较大的缓存。

系统使用缓存索引文件，当服务器按顺序关闭时，该文件会保存到磁盘中。 如果发生电源故障等意外事件，可能无法保存此文件。 此外，可能需要几分钟时间才能 [!DNL Platform Server] 准备好。
