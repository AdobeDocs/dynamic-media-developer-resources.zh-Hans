---
title: 时间戳
description: 文件修改时间戳。 指定上次修改附加到此目录记录的图像和/或数据文件的日期/时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 1%

---

# 时间戳{#timestamp}

文件修改时间戳。 指定上次修改附加到此目录记录的图像和/或数据文件的日期/时间。

如果 `attribute::UseLastModified` 已设置，其中最新 `catalog::TimeStamp` 和 `vignette::TimeStamp` 请求中涉及的所有材质和晕影的值在HTTP响应中作为上次修改的标头返回。

>[!NOTE]
>
>附加到此目录记录的图像或数据文件的实际文件时间绝不会用于此目的。

此 `catalog::TimeStamp` 也用于基于目录的缓存验证(请参阅 [attribute：：CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md))。

## 属性 {#section-42f09e375e72492b87a3a486da7df808}

Java™格式的日期/时间值。 它可以是自午夜1970 UTC/GMT年1月1日以来的整数毫秒数，也可以是具有以下格式之一的日期/时间字符串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* 在0到23之间。
* *[!DNL zzz]* 是一个三或四个字符的时区代码，如“GMT”或“PST”。 夏令时必须在时区代码中说明。 例如，“PST”表示太平洋标准时间，“PDT”表示太平洋夏令时间。
* *[!DNL offset]* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。 例如，“PDT”等同于“GMT -7”。

字符串格式日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，则会忽略该日期/时间值，并且会将 *目录*&#x200B;将改用.ini文件。

## 默认 {#section-e2c126c9e7294662b23944ab8d14866b}

此 `attribute::TimeStamp` 是空的字段或不存在的字段。

## 另请参阅 {#section-876f1d1b50dc4501b605820015a29451}

[attribute：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ， [attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)， [attribute：：CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)， [晕影：：时间戳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
