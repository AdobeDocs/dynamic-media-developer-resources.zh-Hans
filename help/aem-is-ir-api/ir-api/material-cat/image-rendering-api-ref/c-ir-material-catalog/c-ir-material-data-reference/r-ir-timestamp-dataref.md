---
description: 文件修改时间戳。 指定附加到此目录记录的图像和/或数据文件上次修改的日期/时间。
solution: Experience Manager
title: 时间戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 时间戳{#timestamp}

文件修改时间戳。 指定附加到此目录记录的图像和/或数据文件上次修改的日期/时间。

如果 `attribute::UseLastModified` 设置，最近 `catalog::TimeStamp` 和 `vignette::TimeStamp` 请求中涉及的所有材料和晕影的值在HTTP响应中作为上次修改的标头返回。

>[!NOTE]
>
>附加到此目录记录的图像或数据文件的实际文件时间，从不用于此目的。

`catalog::TimeStamp` 也用于基于目录的缓存验证(请参阅 [属性：:CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md))。

## 属性 {#section-42f09e375e72492b87a3a486da7df808}

Java格式的日期/时间值。 可以是自1970年1月1日UTC/GMT午夜以来的整数毫秒数，也可以是使用以下格式之一的日期/时间字符串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* 在0到23之间。
* *[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。 时区代码中必须考虑夏令时（例如，太平洋标准时间为“PST”，太平洋夏令时为“PDT”）。
* *[!DNL offset]* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。 例如，“PDT”等同于“GMT -7”。

字符串格式化日期/时间值的所有元素都必须存在。 如果日期/时间值格式不正确，则会忽略该值，并修改 *目录*.ini文件。

## 默认 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-876f1d1b50dc4501b605820015a29451}

[属性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [属性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [属性：:CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [晕影：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
