---
title: 時間戳記
description: 預設修改時間戳記。 提供目錄TimeStamp和暈映時間戳記的預設值。 如果未指定，則伺服器會使用此catalog.ini檔案的修改日期/時間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---

# 時間戳記{#timestamp}

預設修改時間戳記。 提供預設值 `catalog::TimeStamp` 和 `vignette::TimeStamp`. 如果未指定，則伺服器會使用此catalog.ini檔案的修改日期/時間。

## 屬性 {#section-910e2562b41c47b78ee6216deeabbbd5}

Java™格式的日期/時間值。 可以是自午夜、1970 UTC/GMT年1月1日以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* 介於0到23之間。

*[!DNL zzz]* 是3或4個字元的時區代碼，例如&#39;GMT&#39;或&#39;PST&#39;。 日光節約時間必須在時區代碼中計算（例如，太平洋標準時間為「PST」，而太平洋日光節約時間則為「PDT」）。

*[!DNL offset]* 是相對於GMT的時區位移，單位為小時或小時：分鐘。 例如，「PDT」等於「GMT -7」。

字串格式日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值並修改[！DNL *[!DNL catalog]*&#x200B;已改用.ini]檔案。

## 默认 {#section-65fb29a9ea2044df8cb9fe295eb14872}

如果為空白或未定義，則伺服器會使用此[！DNL]的檔案修改時間 *[!DNL catalog]*.ini]檔案。

## 另请参阅 {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ， [暈映：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)， [attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)， [attribute：：CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
