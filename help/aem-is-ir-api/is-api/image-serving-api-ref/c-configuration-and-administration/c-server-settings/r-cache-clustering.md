---
description: 使用这些服务器设置进行缓存聚类。
solution: Experience Manager
title: 缓存聚类
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# 缓存聚类{#cache-clustering}

使用这些服务器设置进行缓存聚类。

## PS::cacheCluster.hosts — 主机 {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IP地址列表，以分号分隔。 包括此主机应从中获取缓存数据的所有对等服务器的IP地址。 为方便起见，可以包括本地主机的IP地址；这允许群集中所有服务器的配置设置相同。

## PS::cacheCluster.updateLocalCache — 更新本地缓存 {#section-154c2c0af4544200a3499232bb130dde}

如果应将对等服务器提供的缓存条目复制到本地响应缓存，则设置为“是”。

## PS::cacheCluster.queryTimeout — 查询超时 {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

当从对等服务器请求缓存条目时，服务器将等待直到一个服务器做出响应，表示它具有此特定数据项，或者直到所有对等服务器都做出响应，表示它们没有该数据项，或者直到通过此设置指定的时间（以毫秒为单位）过期。

## PS::cacheCluster.fetchTimeout — 获取超时 {#section-41c42a29a26f43dc9cff50ad9fae1f14}

指定服务器将等待从对等服务器传送的实际缓存数据的最大毫秒数。 如果在超时期间之前未提交完整数据，则服务器会假定对等方不可用。 然后，在本地生成缓存条目。
