---
description: 文件修改时间戳。 指定附加到此目录记录的图像和／或数据文件上次修改的日期／时间。
seo-description: 文件修改时间戳。 指定附加到此目录记录的图像和／或数据文件上次修改的日期／时间。
seo-title: 时间戳
solution: Experience Manager
title: 时间戳
topic: Scene7 Image Serving - Image Rendering API
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

文件修改时间戳。 指定附加到此目录记录的图像和／或数据文件上次修改的日期／时间。

如果 `attribute::UseLastModified``catalog::TimeStamp``vignette::TimeStamp` 设置为，则请求中涉及的所有材料和暗角的最新值和值在HTTP响应中作为上次修改的头返回。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>附加到此目录记录的图像或数据文件的实际文件时间永远不用于此目的。

`catalog::TimeStamp` 也用于基于目录的缓存验证(请参 ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`阅)。

## 属性 {#section-42f09e375e72492b87a3a486da7df808}

Java格式的日期／时间值。 可以是自1970年1月1日午夜以来(UTC/GMT)的毫秒数，也可以是日期／时间字符串值（使用以下格式之一）:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]**[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* 介于0到23之间。
* *[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。 夏令时必须在时区代码中计算（例如，“太平洋标准时间”为“PST”，而“太平洋夏令时”为“PDT”）。
* *[!DNL offset]* 是时区相对于GMT的偏移时间（以小时或小时为单位：分钟）。 例如，“PDT”等效于“GMT -7”。

字符串格式化的日期／时间值的所有元素必须存在。 如果日期／时间值的格式不正确，则忽略该值，并改用 *catalog*.ini文件的修改时间。

## 默认 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-876f1d1b50dc4501b605820015a29451}

[属性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ，属 [性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)，属性：:CacheValidationPolicy [,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)[晕影：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
