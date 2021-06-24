---
description: 默认图像修改时间戳。 为目录时间戳提供默认值。
solution: Experience Manager
title: 时间戳
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# 时间戳{#timestamp}

默认图像修改时间戳。 为catalog::TimeStamp提供默认值。

如果未指定，则服务器将使用此&#x200B;[!DNL *`catalog`*.ini]文件的修改日期/时间。

## 属性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期/时间值。 可以是自1970年1月1日UTC/GMT午夜以来的整数毫秒数，也可以是使用以下格式之一的日期/时间字符串值：

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 在0到23之间。

*`zzz`* 是3或4个字符的时区代码，如 `GMT` 或 `PST`。夏令时必须在时区代码(例如，`PST`表示太平洋标准时间，而`PDT`表示太平洋夏令时)。

*`offset`* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。例如， `PDT`等效于`GMT -7`。

字符串格式化日期/时间值的所有元素都必须存在。 如果日期/时间值格式不正确，则忽略该值，并改用&#x200B;[!DNL *`catalog`*.ini]文件的修改时间。

## 默认 {#section-ac465313c97943ed97d41ea852329177}

如果为空或未定义，则服务器将使用此`*`catalog`*.ini`文件的文件修改时间。

## 另请参阅 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
