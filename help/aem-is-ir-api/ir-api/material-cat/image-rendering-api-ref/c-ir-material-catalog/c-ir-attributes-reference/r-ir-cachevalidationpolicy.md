---
title: CacheValidationPolicy
description: 服务器缓存验证策略。 指定验证服务器端缓存条目的时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# CacheValidationPolicy{#cachevalidationpolicy}

服务器缓存验证策略。 指定验证服务器端缓存条目的时间。

通过基于到期的验证，将定期检查源材料和晕影以确定它们是否已更改。 使用基于目录的验证，仅在更改`catalog::TimeStamp`值后检查源图像。

当同时使用材质和晕影目录时，建议使用基于目录的验证。 在图像渲染请求中由路径直接引用晕影时，应使用基于到期的验证。

## 属性 {#section-46e13cb341eb442c86e0d8292de23ea0}

枚举。 0以选择基于到期的验证。 1以选择基于目录的缓存验证。

## 默认 {#section-e09f3af8b6b3497d963199988dc5345d}

如果未定义或为空，则从`default::CacheValidationPolicy`继承。

## 另请参阅 {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog：：时间戳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
