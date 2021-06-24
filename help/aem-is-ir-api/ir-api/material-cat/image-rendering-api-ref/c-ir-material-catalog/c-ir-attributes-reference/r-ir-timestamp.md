---
description: 默认修改时间戳。 为目录时间戳和晕影时间戳提供默认值。 如果未指定，则服务器将使用此catalog.ini文件的修改日期/时间。
solution: Experience Manager
title: 时间戳
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 时间戳{#timestamp}

默认修改时间戳。 为catalog::TimeStamp和晕影：:TimeStamp提供默认值。 如果未指定，则服务器将使用此catalog.ini文件的修改日期/时间。

## 属性 {#section-910e2562b41c47b78ee6216deeabbbd5}

Java格式的日期/时间值。 可以是自1970年1月1日UTC/GMT午夜以来的整数毫秒数，也可以是使用以下格式之一的日期/时间字符串值：

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* 在0到23之间。

*[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。时区代码中必须考虑夏令时（例如，太平洋标准时间为“PST”，太平洋夏令时为“PDT”）。

*[!DNL offset]* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。例如，“PDT”等同于“GMT -7”。

字符串格式化日期/时间值的所有元素都必须存在。 如果日期/时间值格式不正确，则忽略该值，并改用[!DNL *[!DNL catalog]*.ini]文件的修改时间。

## 默认 {#section-65fb29a9ea2044df8cb9fe295eb14872}

如果为空或未定义，则服务器将使用此[!DNL *[!DNL catalog]*.ini]文件的文件修改时间。

## 另请参阅 {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [晕影：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [属性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [属性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
