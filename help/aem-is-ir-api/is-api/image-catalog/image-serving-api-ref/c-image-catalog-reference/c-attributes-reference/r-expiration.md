---
description: 默认客户端缓存的活动时间。 提供默认的过期时间间隔，以防特定目录记录不包含有效的目录过期值。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---


# 过期时间{#expiration}

默认客户端缓存的活动时间。 提供默认的过期时间间隔，以防特定目录记录不包含有效的目录：:Expiration值。

## 属性 {#section-063be3b2f13a48a3a5ab8080718e9812}

实数，0或更大。 自生成回复数据以来到期的小时数。 设置为0可始终立即使回复图像过期，这会有效地禁用客户端缓存。 设置为–1可标记为`never expire`。

## 默认 {#section-f55308b195c04083996f6717c8537634}

如果未定义或为空，则从`default::Expiration`继承。

TTL（生存时间）是缓存过期前的持续时间。 默认TTL为10小时。

## 另请参阅 {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , attribute [::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
