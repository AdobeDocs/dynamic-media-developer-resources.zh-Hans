---
description: 时间戳
solution: Experience Manager
title: 时间戳
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9ce5e42e-573a-4e1c-97d4-98888e16ca56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# TimeStamp{#timestamp}

如果设置`attribute::UseLastModified`，则HTTP响应中的`catalog::TimeStamp`值将作为上次修改的HTTP头返回。 对于静态内容，始终返回“上次修改时间”标头，即使未设置`attribute::UseLastModified`。

对于图像和SVG内容，`catalog::TimeStamp`还用于基于目录的缓存验证（请参阅` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`）。

## 属性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期／时间值。 可以是自1970年1月1日午夜(UTC/GMT)以来的毫秒数，也可以是日期／时间字符串值，其格式如下：

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 在0 - 23范围内。

*`zzz`* 是三到四个字符的时区代码，如“GMT”或“PST”。在时区代码中记录夏令时。 例如，“太平洋标准时间”为“PST”，而“太平洋夏令时”为“PDT”)。

*`offset`* 是时区偏移（以小时为单位）, `hours:minutes`或相对于GMT。例如，“PDT”等效于“GMT -7”。

字符串格式化日期／时间值的所有元素必须存在。 如果日期／时间值格式不正确，则会忽略该值，而改用`*`catalog`*.ini`文件的修改时间。

## 默认 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-c42a427aa4794c548408dc4de028d578}

[属性：:TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [属性：:UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，属 [性：:CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
