---
description: 时间戳
solution: Experience Manager
title: 时间戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# 时间戳{#timestamp}

如果 `attribute::UseLastModified` 设置，则 `catalog::TimeStamp` 值在HTTP响应中作为Last-Modified HTTP标头返回。 对于静态内容，始终返回Last-Modified标头，即使 `attribute::UseLastModified` 未设置。

对于图像和SVG内容， `catalog::TimeStamp` 也用于基于目录的缓存验证(请参阅 [attribute：：CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## 属性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期/时间值。 可以是自午夜1970 UTC/GMT年1月1日以来的毫秒整数，也可以是具有以下格式之一的日期/时间字符串值：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* GMT *`offset`*

*`hh`* 在0到23之间。

*`zzz`* 是一个三或四个字符的时区代码，如“GMT”或“PST”。 在时区代码中计入夏令时。 例如，“PST”表示太平洋标准时间，“PDT”表示太平洋夏令时间)。

*`offset`* 是时区偏移，以小时为单位，或者 `hours:minutes`，相对于GMT。 例如，“PDT”相当于“GMT -7”。

字符串格式日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，则会忽略该值，并且会忽略的修改时间 `*`目录`*.ini` 而使用file。

## 默认 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 如果字段为空或不存在。

## 另请参阅 {#section-c42a427aa4794c548408dc4de028d578}

[attribute：：TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)， [attribute：：UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)， [attribute：：CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
