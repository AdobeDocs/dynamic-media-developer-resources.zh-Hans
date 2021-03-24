---
description: 服务器缓存验证策略。 指定验证服务器端缓存条目的时间。
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

服务器缓存验证策略。 指定验证服务器端缓存条目的时间。

借助基于过期日期的验证，会定期检查源图像是否已更改。 通过基于目录的验证，源图像仅在`catalog::TimeStamp`值更改后才被检查。

使用图像目录时，建议使用基于目录的验证。 在直接引用图像时应使用基于过期的验证，而不使用图像目录。

## 属性 {#section-650cbddd81a24c3b8b70479248a45dc9}

枚举。 0选择基于过期的验证，1选择基于目录的缓存验证。

## 默认 {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

如果未定义或为空，则从`default::CacheValidationPolicy`继承。

## 另请参阅 {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
