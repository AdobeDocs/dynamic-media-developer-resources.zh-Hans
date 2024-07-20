---
title: CacheValidationPolicy
description: 服务器缓存验证策略。 指定验证服务器端缓存条目的时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

服务器缓存验证策略。 指定验证服务器端缓存条目的时间。

通过基于到期的验证，将定期检查源映像是否已更改。 使用基于目录的验证，仅在更改`catalog::TimeStamp`值后检查源图像。

建议在使用图像目录时进行基于目录的验证。 在直接引用图像时，应使用基于到期的验证，而不使用图像目录。

## 属性 {#section-650cbddd81a24c3b8b70479248a45dc9}

枚举。 0表示选择基于到期的验证，1表示选择基于目录的缓存验证。

## 默认 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

如果未定义或为空，则从`default::CacheValidationPolicy`继承。

## 另请参阅 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog：：时间戳](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
