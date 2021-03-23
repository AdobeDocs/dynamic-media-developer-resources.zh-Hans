---
description: 默认图像修改时间戳。 提供目录TimeStamp的默认值。
seo-description: 默认图像修改时间戳。 提供目录TimeStamp的默认值。
seo-title: 时间戳
solution: Experience Manager
title: 时间戳
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# TimeStamp{#timestamp}

默认图像修改时间戳。 提供目录：:TimeStamp的默认值。

如果未指定，服务器将使用此&#x200B;[!DNL *`catalog`*.ini]文件的修改日期/时间。

## 属性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期/时间值。 可以是自午夜（1970年1月1日UTC/GMT）以来的毫秒数，也可以是日期/时间字符串值，其格式如下：

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT  *`offset`*

*`hh`* 在0到23之间。

*`zzz`* 是3或4个字符的时区代码， `GMT` 如 `PST`or夏令时必须在时区代码(例如`PST`表示太平洋标准时间，而`PDT`表示太平洋夏令时)。

*`offset`* 是相对于GMT的时区偏移，以小时或小时：分钟为单位。例如，`PDT`等效于`GMT -7`。

字符串格式日期/时间值的所有元素必须存在。 如果日期/时间值格式不正确，则忽略该值，并改用&#x200B;[!DNL *`catalog`*.ini]文件的修改时间。

## 默认 {#section-ac465313c97943ed97d41ea852329177}

如果为空或未定义，则服务器将使用此`*`catalog`*.ini`文件的文件修改时间。

## 另请参阅 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [属性：:UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，属 [性：:CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
