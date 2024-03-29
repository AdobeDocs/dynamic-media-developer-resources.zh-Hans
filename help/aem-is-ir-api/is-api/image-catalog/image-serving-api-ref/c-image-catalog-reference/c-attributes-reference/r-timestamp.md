---
title: 时间戳
description: 默认图像修改时间戳。 它提供目录TimeStamp的默认值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---

# 时间戳{#timestamp}

默认图像修改时间戳。 提供catalog：：TimeStamp的默认值。

如果未指定，服务器将使用此文件的修改日期/时间 [!DNL *`catalog`*.ini] 文件。

## 属性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期/时间值。 它可以是自午夜1970 UTC/GMT年1月1日以来的整数毫秒数，也可以是具有以下格式之一的日期/时间字符串值：

日期/时间值 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss zzz`*

日期/时间值 *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* GMT *`offset`*

时间值 *`hh`* 在0到23之间。

时间值 *`zzz`* 是三个或四个字符的时区代码，例如 `GMT` 或 `PST`. 夏令时必须计入时区代码(例如， `PST` (太平洋标准时间，与 `PDT` （适用于太平洋夏令时）。

时间值 *`offset`* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。 例如， `PDT` 相当于 `GMT -7`.

字符串格式日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，则会忽略该日期/时间值，并且会将 [!DNL *`catalog`*.ini] 而使用文件。

## 默认 {#section-ac465313c97943ed97d41ea852329177}

如果为空或未定义，则服务器将使用此文件的文件修改时间 `*`目录`*.ini` 文件。

## 另请参阅 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog：：时间戳](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ， [attribute：：UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)， [attribute：：CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
