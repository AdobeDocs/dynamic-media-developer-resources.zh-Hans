---
description: 'null'
seo-description: 'null'
seo-title: 时间戳
solution: Experience Manager
title: 时间戳
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ce5e42e-573a-4e1c-97d4-98888e16ca56
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# TimeStamp{#timestamp}

如果 `attribute::UseLastModified` 设置了此值， `catalog::TimeStamp` 则在HTTP响应中作为上次修改的HTTP头返回该值。 对于静态内容，始终会返回上次修改时间的标题，即使未 `attribute::UseLastModified` 设置也是如此。

对于图像和SVG内容， `catalog::TimeStamp` 还用于基于目录的缓存验证(请参 ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`阅)。

## 属性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期／时间值。 可以是自1970年1月1日午夜以来(UTC/GMT)的毫秒数，也可以是日期／时间字符串值（使用以下格式之一）:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`**`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 在0 - 23的范围内。

*`zzz`* 是“GMT”或“PST”等3或4个字符的时区代码。 在时区代码中帐户夏令时。 例如，“太平洋标准时间”为“PST”,“太平洋夏令时”为“PDT”)。

*`offset`* 是相对于格林尼治时间的时区偏 `hours:minutes`移时间（以小时为单位）。 例如，“PDT”等效于“GMT -7”。

字符串格式化的日期／时间值的所有元素必须存在。 如果日期／时间值格式不正确，则忽略该值，并改用目 ` *`录文件`*.ini` 的修改时间。

## 默认 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 如果字段为空或不存在。

## 另请参阅 {#section-c42a427aa4794c548408dc4de028d578}

[属性：:TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)，属 [性：:UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，属 [性：:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
