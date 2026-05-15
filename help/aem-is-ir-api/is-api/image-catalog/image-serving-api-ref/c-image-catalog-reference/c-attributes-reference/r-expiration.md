---
description: 默认客户端缓存生存时间。 提供特定目录记录中不包含有效目录Expiration值时的默认过期时间间隔。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
TQID: 'https://experienceleague.adobe.com/NkQ-Bj-gHGksaD4Tmt7k8fYVEYfe67ACo4oWS25dKOE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 4%

---

# 過期{#expiration}

默认客户端缓存生存时间。 提供特定目录记录中不包含有效catalog：：Expiration值时的默认过期时间间隔。

## 属性 {#section-063be3b2f13a48a3a5ab8080718e9812}

实数，0或更大。 自生成回复数据以来到到期的小时数。 设置为0将始终使回复图像立即过期，这样可以有效禁用客户端缓存。 设置为–1以标记为`never expire`。

## 默认 {#section-f55308b195c04083996f6717c8537634}

如果未定义或为空，则从`default::Expiration`继承。

TTL （存留期）是缓存过期前的持续时间。 默认TTL为10小时。

## 另请参阅 {#section-b2411d99ddb14115ad475d506efd8967}

[目录：：Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ，[属性：：DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)，[属性：：NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
