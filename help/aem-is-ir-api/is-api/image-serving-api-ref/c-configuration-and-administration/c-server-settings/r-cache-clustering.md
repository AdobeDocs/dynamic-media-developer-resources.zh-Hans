---
description: 使用这些服务器设置进行缓存群集。
seo-description: 使用这些服务器设置进行缓存群集。
seo-title: 缓存群集
solution: Experience Manager
title: 缓存群集
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# 缓存群集{#cache-clustering}

使用这些服务器设置进行缓存群集。

## PS::cacheCluster.hosts —— 主机{#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IP地址列表，以分号分隔。 包括此主机应从中获取缓存数据的所有对等服务器的IP地址。 可以包括本地主机的IP地址，以方便用户；这允许群集中所有服务器的配置设置相同。

## PS::cacheCluster.updateLocalCache —— 更新本地缓存{#section-154c2c0af4544200a3499232bb130dde}

如果应将对等服务器提供的缓存条目复制到本地响应缓存，则设置为“是”。

## PS::cacheCluster.queryTimeout -查询超时{#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

当从对等服务器请求缓存条目时，服务器将等待到一台服务器做出响应，显示该特定数据项，或者直到所有对等服务器都答复它们没有该数据项，或者直到用此设置指定的时间（以毫秒为单位）过期。

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

指定服务器等待从对等服务器传送实际缓存数据的最大毫秒数。 如果超时过期前未传送完整数据，则服务器会假定对等项不可用。 然后在本地生成缓存条目。
