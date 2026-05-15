---
title: 时间戳
description: 默认图像修改时间戳。 它提供目录TimeStamp的默认值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
TQID: 'https://experienceleague.adobe.com/Wyj0OJrb0URsXaymXmx1aB82Qyxun1HatBUqBS4F6cE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 1%

---

# 时间戳{#timestamp}

默认图像修改时间戳。 提供catalog：：TimeStamp的默认值。

如果未指定，服务器将使用此&#x200B;[!DNL *`catalog`*.ini]文件的修改日期/时间。

## 属性 {#section-647066e62ce44a84b627fdd0b2f7cfec}

日期/时间值。 它可以是自午夜1970 UTC/GMT年1月1日以来的整数毫秒数，也可以是具有以下格式之一的日期/时间字符串值：

日期/时间值&#x200B;*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss zzz`*

日期/时间值&#x200B;*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* GMT *`offset`*

时间值&#x200B;*`hh`*&#x200B;在0-23范围内。

时间值&#x200B;*`zzz`*&#x200B;是三或四个字符的时区代码，如`GMT`或`PST`。 夏令时必须在时区代码中说明（例如，太平洋标准时间为`PST`，太平洋夏令时为`PDT`）。

时间值&#x200B;*`offset`*&#x200B;是以小时或小时为单位的时区偏移:minutes，相对于GMT。 例如，`PDT`相当于`GMT -7`。

字符串格式日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，将忽略该值，并改用&#x200B;[!DNL *`catalog`*.ini]文件的修改时间。

## 默认 {#section-ac465313c97943ed97d41ea852329177}

如果为空或未定义，则服务器将使用此`*`目录`*.ini`文件的文件修改时间。

## 另请参阅 {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog：：TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ，[attribute：：UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)，[attribute：：CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
