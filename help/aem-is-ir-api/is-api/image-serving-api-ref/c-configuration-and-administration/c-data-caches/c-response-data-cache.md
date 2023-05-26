---
description: 此 [!DNL Platform Server] 将所有回复图像和某些文本数据缓存到磁盘，除非某个请求标记为不可缓存。
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

此 [!DNL Platform Server] 将所有回复图像和某些文本数据缓存到磁盘，除非某个请求标记为不可缓存。

的位置 [!DNL Platform Server]的磁盘缓存设置为 `PS::cache.rootPaths`.

对于具有高缓存命中率的应用程序，可以通过在多个磁盘设备之间分发响应数据缓存来提高服务器性能和容量。 要完成此操作，请在每个磁盘上创建一个缓存根文件夹，并在中注册它们 `PS::cache.rootPaths`.

`PS::cache.maxSize` 指定所有缓存项的总大小，不考虑任何文件系统开销。 实际需要的磁盘空间量取决于文件系统属性（如磁盘块大小）和缓存条目数。 建议为HTTP磁盘缓存预留的磁盘空间是指定的数量的两倍 `PS::cache.maxSize`. 使用最近最少使用的算法来将缓存的数据量保持在限制内。

除此之外 `PS::cache.maxSize`，则还可以通过限制以下项的缓存条目最大数量来管理响应缓存 `PS::cache.maxEntries`. 在Linux上，此设置必须指定一个不大于缓存分区上可用inode数的值。

>[!NOTE]
>
>此 [!DNL Platform Server] 维护内存中缓存索引。 此索引的大小是32字节乘以的值 `PS::cache.maxEntries`. 您可能需要增加 [!DNL Platform Server] 栈大小，以适应较大的缓存。

当服务器按顺序关闭时，系统将使用保存到磁盘的高速缓存索引文件。 如果发生意外事件（如电源故障），可能无法保存此文件。 此外，可能需要几分钟才能完成 [!DNL Platform Server] 准备好。
