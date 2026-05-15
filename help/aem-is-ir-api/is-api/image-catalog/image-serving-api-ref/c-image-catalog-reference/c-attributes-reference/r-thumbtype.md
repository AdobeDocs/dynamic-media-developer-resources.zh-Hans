---
description: 默认缩略图类型。 提供特定目录记录中不包含有效目录ThumbType值时的缩略图类型默认值。
solution: Experience Manager
title: 缩略图类型
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac29ac3a-8c6b-4c87-954f-37d1ddec76f5
TQID: 'https://experienceleague.adobe.com/BoSwS4iXsvygzR69-5lupAwyynicSlYGRnITnpnSZuc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# 缩略图类型{#thumbtype}

默认缩略图类型。 提供特定目录记录中不包含有效catalog：：ThumbType值时的缩略图类型默认值。

仅用于缩略图请求(`req=tmb`)。

## 属性 {#section-ae0babfe3c8e4c8ebe0124bc55051265}

枚举。 对于&#x200B;*`crop`*、*`fit`*&#x200B;和&#x200B;*`texture`*&#x200B;缩略图类型，允许的值分别为1、2和3。

## 默认 {#section-0237fcae4f304c5b876fceaa839b6b05}

如果未定义或为空，则从`default::ThumbType`继承。

## 另请参阅 {#section-986c97470c494bfd8f179cecf8cc3ccc}

[目录：：ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03)
