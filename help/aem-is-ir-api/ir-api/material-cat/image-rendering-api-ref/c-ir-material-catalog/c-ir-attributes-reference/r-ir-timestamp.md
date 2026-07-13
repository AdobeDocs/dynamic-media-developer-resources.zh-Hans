---
title: 时间戳
description: 默认修改时间戳。 提供目录TimeStamp和晕影TimeStamp的默认值。 如果未指定，服务器将使用此catalog.ini文件的修改日期/时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
TQID: 'https://experienceleague.adobe.com/p3g5NQf25sagtaAYjdd4Vd8J6kZBAoLM8tSY42NPuOI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 7%

---

# 时间戳{#timestamp}

默认修改时间戳。 为`catalog::TimeStamp`和`vignette::TimeStamp`提供默认值。 如果未指定，服务器将使用此catalog.ini文件的修改日期/时间。

## 属性 {#section-910e2562b41c47b78ee6216deeabbbd5}

Java™格式的日期/时间值。 可以是自午夜1970 UTC/GMT年1月1日以来的毫秒整数，也可以是具有以下格式之一的日期/时间字符串值：

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]*&#x200B;在0到23之间。

*[!DNL zzz]*&#x200B;是三或四个字符的时区代码，如“GMT”或“PST”。 夏令时必须在时区代码中说明（例如，太平洋标准时间为“PST”，而太平洋夏令时为“PDT”）。

*[!DNL offset]*&#x200B;是以小时或小时为单位的时区偏移:minutes，相对于GMT。 例如，“PDT”等同于“GMT -7”。

字符串格式日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，将忽略该值，并改用[!DNL *[!DNL catalog]*.ini]文件的修改时间。

## 默认 {#section-65fb29a9ea2044df8cb9fe295eb14872}

如果为空或未定义，则服务器将使用此[!DNL *[!DNL catalog]*.ini]文件的文件修改时间。

## 另请参阅 {#section-764188f9b1734ad1a6270f5fecd28532}

[目录：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ， [晕影：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)，[属性：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)，[属性：：CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)

