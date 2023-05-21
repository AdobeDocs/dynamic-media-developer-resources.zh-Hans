---
description: 檔案修改時間戳記。 指定上次修改附加至此目錄記錄的影像和/或資料檔案的日期/時間。
solution: Experience Manager
title: 時間戳記
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 時間戳記{#timestamp}

檔案修改時間戳記。 指定上次修改附加至此目錄記錄的影像和/或資料檔案的日期/時間。

若 `attribute::UseLastModified` 已設定，最近的 `catalog::TimeStamp` 和 `vignette::TimeStamp` 請求中涉及的所有材質和暈映的值會在HTTP回應中作為上次修改的標頭傳回。

>[!NOTE]
>
>附加至此目錄記錄的影像或資料檔案的實際檔案時間絕不會用於此目的。

`catalog::TimeStamp` 也用於目錄型快取驗證(請參閱 [attribute：：CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md))。

## 屬性 {#section-42f09e375e72492b87a3a486da7df808}

Java格式的日期/時間值。 可以是自午夜、1970 UTC/GMT年1月1日以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*： *[!DNL mm]*： *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* 介於0到23之間。
* *[!DNL zzz]* 是3或4個字元的時區代碼，例如&#39;GMT&#39;或&#39;PST&#39;。 日光節約時間必須在時區代碼中計算（例如，太平洋標準時間為「PST」，而太平洋日光節約時間則為「PDT」）。
* *[!DNL offset]* 是相對於GMT的時區位移，單位為小時或小時：分鐘。 例如，「PDT」等於「GMT -7」。

字串格式日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值並且其修改時間 *目錄*&#x200B;將改用.ini檔案。

## 默认 {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` 欄位是否空白或不存在。

## 另请参阅 {#section-876f1d1b50dc4501b605820015a29451}

[attribute：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ， [attribute：：UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)， [attribute：：CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)， [暈映：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
