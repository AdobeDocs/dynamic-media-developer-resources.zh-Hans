---
title: 时间戳
description: 修改时间戳。 指定上次修改此晕影的日期/时间。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# 时间戳{#timestamp}

修改时间戳。 指定上次修改此晕影的日期/时间。

如果设置`attribute::UseLastModified`，则晕影的最新`vignette::TimeStamp`和`catalog::TimeStamp`值以及请求中涉及的所有材质都将作为last-modified标头返回到HTTP响应中。

>[!NOTE]
>
>从不会将晕影文件的实际文件时间用于此目的。

`catalog::TimeStamp`还用于基于目录的缓存验证。 请参阅[属性：：CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)。

## 属性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java™格式的日期/时间值。 它可以是自午夜1970 UTC/GMT年1月1日以来的整数毫秒数，也可以是具有以下格式之一的日期/时间字符串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]*&#x200B;在0-23范围内。
* *[!DNL zzz]*&#x200B;是三或四个字符的时区代码，如“GMT”或“PST”。 夏令时必须在时区代码中说明（例如，太平洋标准时间为“PST”，而太平洋夏令时为“PDT”）。
* *[!DNL offset]*&#x200B;是相对于GMT的时区偏移，以小时或小时：分钟为单位。 例如，“PDT”等同于“GMT -7”。

字符串格式日期/时间值的所有元素都必须存在。 如果日期/时间值的格式不正确，将忽略该值，并改用[！DNL *[!DNL catalog]*.ini]文件的修改时间。

## 默认 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp`是空或不存在的字段。

## 另请参阅 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ，[catalog：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)，[attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
