---
description: 服务器缓存验证策略。 指定验证服务器端缓存条目的时间。
seo-description: 服务器缓存验证策略。 指定验证服务器端缓存条目的时间。
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

服务器缓存验证策略。 指定验证服务器端缓存条目的时间。

借助基于过期的验证，会定期检查源材料和晕影，以查看它们是否已更改。 使用基于目录的验证，源图像仅在`catalog::TimeStamp`值发生更改后才被检查。

在使用材料目录和暗角目录时，建议进行基于目录的验证。 在图像渲染请求中直接按路径引用晕影时，应使用基于过期的验证。

## 属性 {#section-46e13cb341eb442c86e0d8292de23ea0}

枚举。 0，选择基于过期的验证。 1选择基于目录的缓存验证。

## 默认 {#section-e09f3af8b6b3497d963199988dc5345d}

如果未定义或为空，则从`default::CacheValidationPolicy`继承。

## 另请参阅 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
