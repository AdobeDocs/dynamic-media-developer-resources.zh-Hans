---
description: 默认客户端缓存生存时间。 提供特定目录记录中不包含有效目录Expiration值时的默认过期时间间隔。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---

# 過期{#expiration}

默认客户端缓存生存时间。 提供特定目录记录中不包含有效目录：：Expiration值时的默认过期时间间隔。

## 属性 {#section-063be3b2f13a48a3a5ab8080718e9812}

实数，0或更大。 自生成回复数据后到到期为止的小时数。 设置为0可始终使回复图像立即过期，从而有效地禁用客户端缓存。 设置为–1以标记为 `never expire`.

## 默认 {#section-f55308b195c04083996f6717c8537634}

继承自 `default::Expiration` 如果未定义或为空。

TTL （存留期）是缓存过期前的持续时间。 默认TTL为10小时。

## 另请参阅 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [attribute：：DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)， [attribute：：NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
