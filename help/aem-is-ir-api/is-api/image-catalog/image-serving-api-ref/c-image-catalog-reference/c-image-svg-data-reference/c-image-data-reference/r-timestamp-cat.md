---
title: 时间戳
description: 如果设置了“attribute：：UseLastModified”，则“catalog：：TimeStamp”值将在HTTP响应中作为Last-Modified HTTP标头返回。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
TQID: 'https://experienceleague.adobe.com/Am7JECwqMWbky2JrHKqZV1BJ7ef06JP9Sy-g9uUo8tw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# 时间戳{#timestamp}

如果设置`attribute::UseLastModified`，则HTTP响应中会将`catalog::TimeStamp`值作为Last-Modified HTTP标头返回。 始终为静态内容返回Last-Modified标头，即使未设置`attribute::UseLastModified`也是如此。

对于图像和SVG内容，`catalog::TimeStamp`还用于基于目录的缓存验证（请参阅[attribute：：CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md)）。

## 属性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期/时间值。 可以是自午夜1970 UTC/GMT年1月1日以来的毫秒整数，也可以是具有以下格式之一的日期/时间字符串值：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* GMT *`offset`*

*`hh`*&#x200B;在0到23之间。

*`zzz`*&#x200B;是三或四个字符的时区代码，如“GMT”或“PST”。 以时区代码表示的夏令时帐户。 例如，“PST”表示太平洋标准时间，“PDT”表示太平洋夏令时间)。

*`offset`*&#x200B;是相对于GMT的时区偏移（以小时或`hours:minutes`为单位）。 例如，“PDT”等同于“GMT -7”。

字符串格式化的日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，则会忽略该值，而改用`*`目录`*.ini`文件的修改时间。

## 默认 {#section-0cbf801401ff4857bdda168fd12358af}

如果字段为空或不存在，则为`attribute::TimeStamp`。

## 另请参阅 {#section-c42a427aa4794c548408dc4de028d578}

[属性：：TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)，[属性：：UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，[属性：：CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
