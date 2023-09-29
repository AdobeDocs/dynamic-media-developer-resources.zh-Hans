---
title: 响应数据缓存
description: 此 [!DNL Platform Server] 将所有回复图像和某些文本数据缓存到磁盘，除非请求标记为不可缓存。
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

此 [!DNL Platform Server] 将所有回复图像和某些文本数据缓存到磁盘，除非请求标记为不可缓存。

的位置 [!DNL Platform Server]的磁盘缓存设置为 `PS::cache.rootPaths`.

对于具有高缓存命中率的应用程序，可以通过在多个磁盘设备之间分发响应数据缓存来提高服务器性能和容量。 要完成此操作，请在每个磁盘上创建缓存根文件夹，并在中注册它们 `PS::cache.rootPaths`.

此 `PS::cache.maxSize` 指定所有缓存项的总大小，不考虑任何文件系统开销。 所需的磁盘空间量取决于文件系统属性（如磁盘块大小）和缓存条目数。 为HTTP磁盘缓存保留的磁盘空间是指定的容量的两倍 `PS::cache.maxSize`. 使用最近最少使用的算法来使缓存的数据量保持在限制之内。

此外 `PS::cache.maxSize`，则响应缓存也可通过以下方式管理：限制最大缓存条目数 `PS::cache.maxEntries`. 在Linux®上，此设置指定的值不能大于缓存分区上可用的inode数。

>[!NOTE]
>
>此 [!DNL Platform Server] 维护内存中缓存索引。 此索引的大小是32字节乘以值 `PS::cache.maxEntries`. 增加 [!DNL Platform Server] 栈大小，以适应较大的缓存（如有必要）。

当服务器按顺序关闭时，系统将使用保存到磁盘的高速缓存索引文件。 如果发生意外事件（如电源故障），则可能无法保存此文件。 此外，可能需要几分钟才能完成 [!DNL Platform Server] 准备好。
