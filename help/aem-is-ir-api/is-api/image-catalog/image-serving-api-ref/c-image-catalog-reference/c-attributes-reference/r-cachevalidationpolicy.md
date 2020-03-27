---
description: 服务器缓存验证策略。 指定何时验证服务器端缓存条目。
seo-description: 服务器缓存验证策略。 指定何时验证服务器端缓存条目。
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 371dadbf-d58e-4214-8050-7e8907b436e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

服务器缓存验证策略。 指定何时验证服务器端缓存条目。

借助基于过期的验证，系统会定期检查源图像是否已更改。 使用基于目录的验证，源图像仅在值更改后 `catalog::TimeStamp` 才被检查。

使用图像目录时，建议使用基于目录的验证。 在直接引用图像时应使用基于过期的验证，而不使用图像目录。

## 属性 {#section-650cbddd81a24c3b8b70479248a45dc9}

枚举。 0选择基于过期的验证，1选择基于目录的缓存验证。

## 默认 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

如果未定义 `default::CacheValidationPolicy` 或为空，则从中继承。

## 另请参阅 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
