---
description: 使用这些服务器设置进行缓存群集。
solution: Experience Manager
title: 缓存聚类
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 缓存聚类{#cache-clustering}

使用这些服务器设置进行缓存群集。

## PS：：cacheCluster.hosts — 主机 {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

IP地址列表，以分号分隔。 包括此主机应从中获取缓存数据的所有对等服务器的IP地址。 为了方便起见，可以包含本地主机的IP地址；这样允许群集中的所有服务器具有相同的配置设置。

## PS：：cacheCluster.updateLocalCache — 更新本地缓存 {#section-154c2c0af4544200a3499232bb130dde}

如果将对等服务器提供的缓存项复制到本地响应缓存，则设置为“是”。

## PS：：cacheCluster.queryTimeout — 查询超时 {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

当从对等服务器请求缓存项时，服务器将等待一个服务器响应它有此特定数据项，或等待所有对等服务器响应它们没有此数据项，或等待使用此设置指定的时间（以毫秒为单位）过期。

## PS：：cacheCluster.fetchTimeout — 获取超时 {#section-41c42a29a26f43dc9cff50ad9fae1f14}

指定服务器等待从对等服务器传送实际缓存数据的最大毫秒数。 如果在超时过期之前未提交完整数据，则服务器会假定对等节点已变为不可用。 然后，在本地生成缓存项。
