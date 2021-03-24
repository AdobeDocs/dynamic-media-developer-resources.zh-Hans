---
description: 非映像响应的客户端缓存TTL。 提供某些非图像响应的过期时间间隔。
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---


# NonImgExpiration{#nonimgexpiration}

非映像响应的客户端缓存TTL。 提供某些非图像响应的过期时间间隔。

提供某些非图像响应的过期间隔，包括响应以下命令发送的响应：

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 属性 {#section-d37e3113f4b1468b86b5a14e80d94c83}

实数，0或更大。 自生成回复数据以来到期的小时数。 设置为0可始终立即使回复图像过期，这会有效地禁用默认图像响应的客户端缓存。 设置为–1将标记为&#x200B;*永不过期*。

## 默认 {#section-96981360c0234b7f824d2ff7c25a7954}

如果未定义或为空，则从`default::NonImgExpiration`继承。

TTL（生存时间）是缓存过期前的持续时间。 默认TTL为6分钟。

## 另请参阅 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
