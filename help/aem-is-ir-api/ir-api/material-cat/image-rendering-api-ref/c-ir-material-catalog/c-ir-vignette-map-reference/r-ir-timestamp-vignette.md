---
description: 修改时间戳。 指定上次修改此晕影的日期/时间。
solution: Experience Manager
title: 时间戳
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 时间戳{#timestamp}

修改时间戳。 指定上次修改此晕影的日期/时间。

如果 `attribute::UseLastModified` 已设置，最近 `vignette::TimeStamp` 和 `catalog::TimeStamp`晕影的值和请求中涉及的所有材料将在HTTP响应中作为上次修改的标头返回。

>[!NOTE]
>
>晕影文件的实际文件时间从不用于此目的。

`catalog::TimeStamp` 也用于基于目录的缓存验证(请参阅 [属性：:CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## 属性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java格式的日期/时间值。 可以是自1970年1月1日UTC/GMT午夜以来的整数毫秒数，也可以是使用以下格式之一的日期/时间字符串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*:*[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* 在0到23之间。
* *[!DNL zzz]* 是3或4个字符的时区代码，如“GMT”或“PST”。 时区代码中必须考虑夏令时（例如，太平洋标准时间为“PST”，太平洋夏令时为“PDT”）。
* *[!DNL offset]* 是以小时或小时：分钟为单位的时区偏移，相对于GMT。 例如，“PDT”等同于“GMT -7”。

字符串格式化日期/时间值的所有元素都必须存在。 如果日期/时间值格式不正确，则会忽略该值，并且会忽略[!DNL的修改时间 *[!DNL catalog]*.ini]文件。

## 默认 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` 字段为空或不存在。

## 另请参阅 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[属性：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [属性：:UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
