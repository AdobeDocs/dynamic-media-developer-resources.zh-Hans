---
description: 默认缩略图类型。 提供特定目录记录中不包含有效目录ThumbType值时的缩略图类型默认值。
solution: Experience Manager
title: 缩略图类型
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac29ac3a-8c6b-4c87-954f-37d1ddec76f5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
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
