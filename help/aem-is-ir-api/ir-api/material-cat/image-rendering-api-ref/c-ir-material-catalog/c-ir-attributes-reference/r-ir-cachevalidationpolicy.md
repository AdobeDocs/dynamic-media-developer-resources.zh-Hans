---
description: 服务器缓存验证策略。 指定验证服务器端缓存条目的时间。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

服务器缓存验证策略。 指定验证服务器端缓存条目的时间。

通过基于过期的验证，将定期检查源材料和晕影，以查看它们是否已更改。 通过基于目录的验证，源图像仅在`catalog::TimeStamp`值发生更改后才会被检查。

同时使用材料和晕影目录时，建议进行基于目录的验证。 当路径直接在图像渲染请求中引用晕影时，应使用基于过期的验证。

## 属性 {#section-46e13cb341eb442c86e0d8292de23ea0}

枚举。 0来选择基于过期的验证。 1选择基于目录的缓存验证。

## 默认 {#section-e09f3af8b6b3497d963199988dc5345d}

从`default::CacheValidationPolicy`继承（如果未定义或为空）。

## 另请参阅 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
