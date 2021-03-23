---
description: 文件修改时间戳。 指定附加到此目录记录的图像和/或数据文件上次修改的日期/时间。
seo-description: 文件修改时间戳。 指定附加到此目录记录的图像和/或数据文件上次修改的日期/时间。
seo-title: 时间戳
solution: Experience Manager
title: 时间戳
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---


# TimeStamp{#timestamp}

文件修改时间戳。 指定附加到此目录记录的图像和/或数据文件上次修改的日期/时间。

如果设置`attribute::UseLastModified`，则所有材料的`catalog::TimeStamp`和`vignette::TimeStamp`值以及请求中涉及的晕影的最近值作为上次修改的标头在HTTP响应中返回。

>[!NOTE]
>
>附加到此目录记录的图像或数据文件的实际文件时间永远不会用于此目的。

`catalog::TimeStamp` 还用于基于目录的缓存验证(请参阅 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`)。

## 属性 {#section-42f09e375e72492b87a3a486da7df808}

Java格式的日期/时间值。 可以是自午夜（1970年1月1日UTC/GMT）以来的毫秒数，也可以是日期/时间字符串值，其格式如下：

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* 在0到23之间。
* *[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。夏令时必须在时区代码中计算（例如，太平洋标准时间为“PST”，而太平洋夏令时为“PDT”）。
* *[!DNL offset]* 是相对于GMT的时区偏移，以小时或小时：分钟为单位。例如，“PDT”等效于“GMT -7”。

字符串格式日期/时间值的所有元素必须存在。 如果日期/时间值格式不正确，则忽略该值，并改用&#x200B;*catalog*.ini文件的修改时间。

## 默认 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-876f1d1b50dc4501b605820015a29451}

[属性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ，属 [性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)，属 [性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [晕影：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
