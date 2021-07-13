---
description: 默认图像响应的客户端缓存TTL。 提供默认图像响应的过期时间间隔（返回使用defaultImage=或属性DefaultImage指定的默认图像的响应）。
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# DefaultExpiration{#defaultexpiration}

默认图像响应的客户端缓存TTL。 提供默认图像响应的过期时间间隔（返回使用defaultImage=或attribute::DefaultImage指定的默认图像的响应）。

仅当默认图像与目录记录无关联，或默认图像目录记录不提供特定`catalog::Expiration`值时才应用。

## 属性 {#section-e564512476604fd7b964f9f2903d6d33}

实数，0或更大。 自生成回复数据后到期的小时数。 设置为0时，将始终立即使回复图像过期，这会有效地禁用默认图像响应的客户端缓存。 设置为`-1`以标记为`never expire`。

## 默认 {#section-131cd32c2e214391857dba5af321f8cd}

从`default::DefaultExpiration`继承（如果未定义或为空）。

TTL（生存时间）是缓存过期前的持续时间。 默认TTL为1小时。

## 另请参阅 {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
