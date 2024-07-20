---
title: 過期
description: 默认客户端缓存生存时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---

# 過期{#expiration}

默认客户端缓存生存时间。 提供特定目录记录中不包含有效`catalog::Expiration`或`vignette::Expiration`值时的默认过期时间间隔。 或者，如果直接访问晕影文件或材料文件，而不是通过目录记录访问。

## 属性 {#section-8e2bade105ec4905ae5c4911f500279f}

实数，`0`或更大。 自生成回复数据以来到到期的小时数。 设置为`0`将始终使回复图像立即过期，这样可以有效禁用客户端缓存。 设置为`-1`以标记为&#x200B;*永不过期*。

## 默认 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

如果未定义或为空，则从`default::Expiration`继承。

## 另请参阅 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[目录：：过期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)，[晕影：：过期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
