---
description: 默认图像修改时间戳。 为目录TimeStamp提供默认值。
seo-description: 默认图像修改时间戳。 为目录TimeStamp提供默认值。
seo-title: 时间戳
solution: Experience Manager
title: 时间戳
topic: Scene7 Image Serving - Image Rendering API
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

默认图像修改时间戳。 为catalog::TimeStamp提供默认值。

如果未指定，则服务器将使用此。ini文件的修改日期/ [!DNL *`catalog`*时间] 。

## 属性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期／时间值。 可以是自1970年1月1日午夜以来(UTC/GMT)的毫秒数，也可以是日期／时间字符串值（使用以下格式之一）:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

*`mm`*/ *`dd`*/ *`yyyy`**`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* 介于0到23之间。

*`zzz`* 是3或4个字符的时区代码， `GMT` 如或 `PST`夏令时必须在时区代码中计算(例如，对 `PST` 于太平洋标准时间，对于太平洋夏令时 `PDT` 间)。

*`offset`* 是时区相对于GMT的偏移时间（以小时或小时为单位：分钟）。 例如， `PDT` 等效于 `GMT -7`。

字符串格式化的日期／时间值的所有元素必须存在。 如果日期／时间值格式不正确，则忽略该值，并改用 [!DNL *`catalog`*.ini文件的修改时间] 。

## 默认 {#section-ac465313c97943ed97d41ea852329177}

如果为空或未定义，则服务器将使用此目录文件的文件修改 ` *`时间`*.ini` 。

## 另请参阅 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ，属 [性：:UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，属 [性：:CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
