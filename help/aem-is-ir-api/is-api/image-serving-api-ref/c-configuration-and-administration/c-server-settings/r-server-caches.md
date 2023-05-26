---
description: 将这些服务器设置用于服务器缓存。
solution: Experience Manager
title: 服务器缓存
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 服务器缓存{#server-caches}

将这些服务器设置用于服务器缓存。

## PS：：cache.rootPaths — 缓存数据文件夹 {#section-f0aa808304d74ecdb0c3644f11906c53}

的根文件夹 [!DNL Platform Server]的磁盘缓存。 一个或多个绝对文件路径或相对于 *[!DNL install_folder]*，以分号(；)分隔。 HTTP响应缓存的数据均匀地分布在所有指定的文件夹中。 辅助高速缓存（编译的图像目录和外来图像数据）的高速缓存位于主高速缓存文件夹（列表中的第一个文件夹）中。

## PS：：cache.maxSize — 响应数据缓存大小 {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

HTTP响应缓存的最大大小（字节）。 此设置限制要缓存的实际数据量；不考虑文件系统开销。 (请参阅 [响应数据缓存](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) 如果指定了多个缓存数据文件夹，则缓存数据会平均分布在所有文件夹中。 的值 `cache.maxSize` 在 [!DNL PlatformServer.conf] 以字节为单位。

## PS：：cache.maxEntries — 响应数据缓存最大条目数 {#section-5603e327e90542a5b50aeeb27b080410}

为内存中HTTP响应缓存索引分配的条目数。

>[!NOTE]
>
>在Linux上，确保为缓存分区分配了足够的i-node ，以避免i-node用完。

## IS：：TempDirectory — 图像服务器临时文件文件夹 {#section-42ea1e7a68c444878f7245c5bbcb1672}

图像服务器有时需要将中间数据保存到磁盘。 路径可以是绝对路径或相对路径 *[!DNL install_folder]*.

>[!NOTE]
>
>在更改此设置之前，必须创建新文件夹。 确保设置了访问权限，以便图像服务器完全控制文件夹。

## SV：：temp — 服务器主管临时文件文件夹 {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

服务器管理员有时需要将中间数据保存到磁盘。 路径可以是绝对路径或相对路径 *[!DNL install_folder]*. 默认为[！DNL  *[!DNL install_folder]*/temp]。

>[!NOTE]
>
>在更改此设置之前，必须创建新文件夹。 确保设置了访问权限，以便Server Supervisor完全控制文件夹。
