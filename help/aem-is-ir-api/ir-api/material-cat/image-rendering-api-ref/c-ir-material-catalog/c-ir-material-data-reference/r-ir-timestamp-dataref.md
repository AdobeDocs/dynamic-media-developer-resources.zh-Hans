---
description: 文件修改时间戳。 指定附加到此目录记录的图像和/或数据文件上次修改的日期/时间。
solution: Experience Manager
title: 时间戳
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 1%

---

# 时间戳{#timestamp}

文件修改时间戳。 指定附加到此目录记录的图像和/或数据文件上次修改的日期/时间。

如果设置了`attribute::UseLastModified`，则在HTTP响应中作为上次修改的标头返回所有材料和请求中涉及的晕影的`catalog::TimeStamp`和`vignette::TimeStamp`值的最新值。

>[!NOTE]
>
>附加到此目录记录的图像或数据文件的实际文件时间，从不用于此目的。

`catalog::TimeStamp` 也用于基于目录的缓存验证(请参阅 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`)。

## 属性 {#section-42f09e375e72492b87a3a486da7df808}

Java格式的日期/时间值。 可以是自1970年1月1日UTC/GMT午夜以来的整数毫秒数，也可以是使用以下格式之一的日期/时间字符串值：

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* 在0到23之间。
* *[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。时区代码中必须考虑夏令时（例如，太平洋标准时间为“PST”，太平洋夏令时为“PDT”）。
* *[!DNL offset]* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。例如，“PDT”等同于“GMT -7”。

字符串格式化日期/时间值的所有元素都必须存在。 如果日期/时间值格式不正确，则忽略该值，并改用&#x200B;*catalog*.ini文件的修改时间。

## 默认 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-876f1d1b50dc4501b605820015a29451}

[属性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [属性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [属性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4),  [Vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
