---
description: 默认图像响应的客户端缓存TTL。 提供默认图像响应（返回使用defaultImage=或属性DefaultImage指定的默认图像的响应）的过期时间间隔。
seo-description: 默认图像响应的客户端缓存TTL。 提供默认图像响应（返回使用defaultImage=或属性DefaultImage指定的默认图像的响应）的过期时间间隔。
seo-title: 默认过期
solution: Experience Manager
title: 默认过期
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# DefaultExpiration{#defaultexpiration}

默认图像响应的客户端缓存TTL。 提供默认图像响应（返回使用defaultImage=或attribute:DefaultImage指定的默认图像的响应）的过期时间间隔。

仅当默认图像未与目录记录关联或默认图像目录记录未提供特定`catalog::Expiration`值时应用。

## 属性 {#section-e564512476604fd7b964f9f2903d6d33}

实数，0或更大。 自生成回复数据后，到期的小时数。 设置为0以始终立即使回复图像过期，这会有效地禁用默认图像响应的客户端缓存。 设置为`-1`以标记为`never expire`。

## 默认 {#section-131cd32c2e214391857dba5af321f8cd}

如果未定义或为空，则从`default::DefaultExpiration`继承。

TTL（生存时间）是缓存过期前的持续时间。 默认TTL为1小时。

## 另请参阅 {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
