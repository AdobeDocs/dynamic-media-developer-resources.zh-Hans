---
title: 时间戳
description: 默认修改时间戳。 为目录TimeStamp和晕影TimeStamp提供默认值。 如果未指定，服务器将使用此catalog.ini文件的修改日期/时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---

# 时间戳{#timestamp}

默认修改时间戳。 提供默认值 `catalog::TimeStamp` 和 `vignette::TimeStamp`. 如果未指定，服务器将使用此catalog.ini文件的修改日期/时间。

## 属性 {#section-910e2562b41c47b78ee6216deeabbbd5}

Java™格式的日期/时间值。 可以是自午夜1970 UTC/GMT年1月1日以来的毫秒整数，也可以是具有以下格式之一的日期/时间字符串值：

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* 在0到23之间。

*[!DNL zzz]* 是一个三或四个字符的时区代码，如“GMT”或“PST”。 夏令时必须在时区代码中记录（例如，太平洋标准时间为“PST”，太平洋夏令时为“PDT”）。

*[!DNL offset]* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。 例如，“PDT”相当于“GMT -7”。

字符串格式日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，则会忽略该值，并忽略[！DNL]的修改时间 *[!DNL catalog]*&#x200B;将改用.ini]文件。

## 默认 {#section-65fb29a9ea2044df8cb9fe295eb14872}

如果为空或未定义，则服务器将使用此[！DNL]的文件修改时间 *[!DNL catalog]*.ini]文件。

## 另请参阅 {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog：：时间戳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ， [晕影：：时间戳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)， [attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)， [attribute：：CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
