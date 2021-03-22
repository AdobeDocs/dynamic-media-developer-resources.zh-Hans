---
description: 修改时间戳。 指定上次修改此晕影的日期/时间。
seo-description: 修改时间戳。 指定上次修改此晕影的日期/时间。
seo-title: 时间戳
solution: Experience Manager
title: 时间戳
uuid: d2649e86-8a6f-4f63-ab6a-8b2d8c03f8c0
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# TimeStamp{#timestamp}

修改时间戳。 指定上次修改此晕影的日期/时间。

如果设置`attribute::UseLastModified`，则在HTTP响应中作为上次修改的标头返回晕影的最近`vignette::TimeStamp`和`catalog::TimeStamp`值以及请求中涉及的所有材料。

>[!NOTE]
>
>晕影文件的实际文件时间永远不会用于此目的。

`catalog::TimeStamp` 还用于基于目录的缓存验证(请参阅 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`)。

## 属性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java格式的日期/时间值。 可以是自午夜（1970年1月1日UTC/GMT）以来的毫秒数，也可以是日期/时间字符串值，其格式如下：

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:*[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* 在0到23之间。
* *[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。夏令时必须在时区代码中计算（例如，太平洋标准时间为“PST”，而太平洋夏令时为“PDT”）。
* *[!DNL offset]* 是相对于GMT的时区偏移，以小时或小时：分钟为单位。例如，“PDT”等效于“GMT -7”。

字符串格式日期/时间值的所有元素必须存在。 如果日期/时间值格式不正确，则忽略该值，并将改用[!DNL *[!DNL catalog]*.ini]文件的修改时间。

## 默认 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute:::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319),  [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
