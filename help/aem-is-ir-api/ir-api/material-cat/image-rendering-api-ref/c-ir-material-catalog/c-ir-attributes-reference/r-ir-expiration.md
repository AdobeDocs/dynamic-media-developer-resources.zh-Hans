---
title: 過期
description: 默认的客户端缓存生存时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 5%

---

# 過期{#expiration}

默认的客户端缓存生存时间。 提供默认过期时间间隔，以防特定目录记录不包含有效的 `catalog::Expiration` 或 `vignette::Expiration` 值。 或者，如果直接访问晕影文件或材料文件，而不是通过目录记录。

## 属性 {#section-8e2bade105ec4905ae5c4911f500279f}

实数， `0` 或更大。 自生成回复数据后到期的小时数。 设置为 `0` 始终立即使回复图像过期，这会有效地禁用客户端缓存。 设置为 `-1` 标记为 *永不过期*.

## 默认 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

继承自 `default::Expiration` 如果未定义或为空。

## 另请参阅 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[目录：：过期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [晕影：：过期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
