---
description: 非图像响应的客户端缓存TTL。 提供某些非图像响应的过期时间间隔。
solution: Experience Manager
title: 非图像过期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# 非图像过期{#nonimgexpiration}

非图像响应的客户端缓存TTL。 提供某些非图像响应的过期时间间隔。

为某些非图像响应（包括响应以下命令发送的响应）提供过期时间间隔：

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 属性 {#section-d37e3113f4b1468b86b5a14e80d94c83}

实数，0或更大。 自生成回复数据后到到期为止的小时数。 设置为0可始终使回复图像立即过期，这样可以有效禁用默认图像响应的客户端缓存。 设置为–1以标记为 *永不过期*.

## 默认 {#section-96981360c0234b7f824d2ff7c25a7954}

继承自 `default::NonImgExpiration` 如果未定义或为空。

TTL （存留期）是缓存过期前的持续时间。 默认TTL为6分钟。

## 另请参阅 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [attribute：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
