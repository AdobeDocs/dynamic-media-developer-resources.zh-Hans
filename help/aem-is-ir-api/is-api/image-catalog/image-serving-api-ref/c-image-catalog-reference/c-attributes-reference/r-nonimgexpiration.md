---
description: 非图像响应的客户端缓存TTL。 提供某些非映像响应的过期时间间隔。
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
TQID: 'https://experienceleague.adobe.com/A21KkwsYFIMp9Pw0WyX-c-3UVlFg2FacObh2jjRVTwA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

非图像响应的客户端缓存TTL。 提供某些非映像响应的过期时间间隔。

提供某些非映像响应的过期时间间隔，包括响应以下命令发送的响应：

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## 属性 {#section-d37e3113f4b1468b86b5a14e80d94c83}

实数，0或更大。 自生成回复数据以来到到期的小时数。 设置为0将始终使回复图像立即过期，这样可以有效禁用默认图像响应的客户端缓存。 设置为–1以标记为&#x200B;*永不过期*。

## 默认 {#section-96981360c0234b7f824d2ff7c25a7954}

如果未定义或为空，则从`default::NonImgExpiration`继承。

TTL （存留期）是缓存过期前的持续时间。 默认TTL为6分钟。

## 另请参阅 {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[目录：：Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [属性：：DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
