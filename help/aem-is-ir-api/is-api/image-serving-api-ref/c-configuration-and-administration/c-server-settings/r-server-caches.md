---
description: 对服务器缓存使用这些服务器设置。
seo-description: 对服务器缓存使用这些服务器设置。
seo-title: 服务器缓存
solution: Experience Manager
title: 服务器缓存
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# 服务器缓存{#server-caches}

对服务器缓存使用这些服务器设置。

## PS::cache.rootPaths —— 缓存数据文件夹 {#section-f0aa808304d74ecdb0c3644f11906c53}

平台服务器的磁盘缓存的根文件夹。 一个或多个相对的绝对文件路径或路径， *[!DNL install_folder]*&#x200B;以分号(;)分隔。 HTTP响应缓存的数据将平均分布于所有指定文件夹。 辅助高速缓存（编译的图像目录和外部图像数据）的高速缓存将位于主高速缓存文件夹(列表中的第一个文件夹)中。

## PS::cache.maxSize —— 响应数据缓存大小 {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP响应缓存的最大大小（以字节为单位）。 此设置限制了实际缓存的数据量； 它不考虑文件系统开销。 (请参 [阅响应数据缓存](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca)。) 如果指定了多个缓存数据文件夹，缓存数据将平均分布在所有文件夹中。 值(以字 `cache.maxSize` 节 [!DNL PlatformServer.conf] 为单位)。

## PS::cache.maxEntries —— 响应数据缓存最大条目数 {#section-5603e327e90542a5b50aeeb27b080410}

为内存中HTTP响应缓存索引分配的条目数。

>[!NOTE]
>
>在Linux上，确保为缓存分区分配了足够的i节点，以避免i节点耗尽。

## IS::TempDirectory - Image Server临时文件文件夹 {#section-42ea1e7a68c444878f7245c5bbcb1672}

图像服务器偶尔需要将中间数据保存到磁盘。 路径可以是绝对路径，也可以是相对路径 *[!DNL install_folder]*。

>[!NOTE]
>
>必须在更改此设置之前创建新文件夹。 确保已设置访问权限，以便图像服务器能够完全控制文件夹。

## SV::temp —— 服务器主管临时文件文件夹 {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

服务器管理者偶尔需要将中间数据保存到磁盘。 路径可以是绝对路径，也可以是相对路径 *[!DNL install_folder]*。 默认为[!DNL *[!DNL install_folder]*/temp]。

>[!NOTE]
>
>必须在更改此设置之前创建新文件夹。 确保已设置访问权限，以便服务器主管能够完全控制文件夹。

