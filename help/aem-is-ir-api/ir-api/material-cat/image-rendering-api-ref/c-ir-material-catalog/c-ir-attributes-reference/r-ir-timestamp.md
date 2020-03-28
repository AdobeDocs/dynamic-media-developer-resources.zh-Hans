---
description: 默认修改时间戳。 为目录TimeStamp和晕影TimeStamp提供默认值。 如果未指定，则服务器将使用此catalog.ini文件的修改日期／时间。
seo-description: 默认修改时间戳。 为目录TimeStamp和晕影TimeStamp提供默认值。 如果未指定，则服务器将使用此catalog.ini文件的修改日期／时间。
seo-title: 时间戳
solution: Experience Manager
title: 时间戳
topic: Scene7 Image Serving - Image Rendering API
uuid: 10ceb600-1ed9-46a1-ae07-889d601ac0f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

默认修改时间戳。 提供目录：:TimeStamp和暗角：:TimeStamp的默认值。 如果未指定，则服务器将使用此catalog.ini文件的修改日期／时间。

## 属性 {#section-910e2562b41c47b78ee6216deeabbbd5}

Java格式的日期／时间值。 可以是自1970年1月1日午夜以来(UTC/GMT)的毫秒数，也可以是日期／时间字符串值（使用以下格式之一）:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]**[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* 介于0到23之间。

*[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。 夏令时必须在时区代码中计算（例如，“太平洋标准时间”为“PST”，而“太平洋夏令时”为“PDT”）。

*[!DNL offset]* 是时区相对于GMT的偏移时间（以小时或小时为单位：分钟）。 例如，“PDT”等效于“GMT -7”。

字符串格式化的日期／时间值的所有元素必须存在。 如果日期／时间值的格式不正确，则忽略该值，并将改用[!DNL *[!DNL catalog]*.ini]文件的修改时间。

## 默认 {#section-65fb29a9ea2044df8cb9fe295eb14872}

如果为空或未定义，则服务器将使用此[!DNL.ini]文件的文件修 *[!DNL catalog]*&#x200B;改时间。

## 另请参阅 {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [暗角：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)，属 [性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [属性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
