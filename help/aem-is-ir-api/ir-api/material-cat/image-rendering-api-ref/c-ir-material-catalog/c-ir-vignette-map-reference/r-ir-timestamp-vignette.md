---
description: 修改時間戳記。 指定上次修改此暈映的日期/時間。
solution: Experience Manager
title: 時間戳記
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 時間戳記{#timestamp}

修改時間戳記。 指定上次修改此暈映的日期/時間。

若 `attribute::UseLastModified` 已設定，最近 `vignette::TimeStamp` 和 `catalog::TimeStamp`請求中涉及的暈映和所有素材的值會在HTTP回應中作為上次修改的標頭傳回。

>[!NOTE]
>
>暈映檔案的實際檔案時間絕不會用於此目的。

`catalog::TimeStamp` 也用於目錄型快取驗證(請參閱 [attribute：：CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## 屬性 {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Java格式的日期/時間值。 可以是自午夜、1970 UTC/GMT年1月1日以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* 介於0到23之間。
* *[!DNL zzz]* 是3或4個字元的時區代碼，例如&#39;GMT&#39;或&#39;PST&#39;。 日光節約時間必須在時區代碼中計算（例如，太平洋標準時間為「PST」，而太平洋日光節約時間則為「PDT」）。
* *[!DNL offset]* 是相對於GMT的時區位移，單位為小時或小時：分鐘。 例如，「PDT」等於「GMT -7」。

字串格式日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值以及[！DNL]的修改時間 *[!DNL catalog]*&#x200B;已改用.ini]檔案。

## 默认 {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` 欄位是否空白或不存在。

## 另请参阅 {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ， [catalog：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)， [attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
