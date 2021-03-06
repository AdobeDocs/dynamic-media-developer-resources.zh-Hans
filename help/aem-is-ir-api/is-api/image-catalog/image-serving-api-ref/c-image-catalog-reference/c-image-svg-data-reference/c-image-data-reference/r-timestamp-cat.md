---
description: 时间戳
solution: Experience Manager
title: 时间戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# 时间戳{#timestamp}

如果 `attribute::UseLastModified` 设置时， `catalog::TimeStamp` 值在HTTP响应中作为上次修改的HTTP标头返回。 对于静态内容，始终返回Last-Modified标头，即使 `attribute::UseLastModified` 未设置。

对于图像和SVG内容， `catalog::TimeStamp` 也用于基于目录的缓存验证(请参阅 [属性：:CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## 属性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期/时间值。 可以是自1970年1月1日UTC/GMT午夜以来的整数毫秒数，也可以是使用以下格式之一的日期/时间字符串值：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 在0 - 23范围内。

*`zzz`* 是三个或四个字符的时区代码，如“GMT”或“PST”。 在时区代码中考虑夏令时。 例如，太平洋标准时间为“PST”，而太平洋夏令时为“PDT”)。

*`offset`* 是以小时或 `hours:minutes`，相对于GMT。 例如，“PDT”等同于“GMT -7”。

字符串格式化日期/时间值的所有元素都必须存在。 如果日期/时间值格式不正确，则会忽略该值，并修改 `*`目录`*.ini` 文件。

## 默认 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-c42a427aa4794c548408dc4de028d578}

[属性：:TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [属性：:UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [属性：:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
