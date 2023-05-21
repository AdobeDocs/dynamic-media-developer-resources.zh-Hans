---
description: 時間戳記
solution: Experience Manager
title: 時間戳記
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# 時間戳記{#timestamp}

若 `attribute::UseLastModified` 已設定，則 `catalog::TimeStamp` 值會以Last-Modified HTTP標頭的形式傳回HTTP回應。 系統會一律為靜態內容傳回Last-Modified標頭，即使 `attribute::UseLastModified` 未設定。

針對影像和SVG內容， `catalog::TimeStamp` 也用於目錄型快取驗證(請參閱 [attribute：：CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## 屬性 {#section-2298a384b5cb43929542655c5a49beb2}

Java格式的日期/時間值。 可以是自午夜、1970 UTC/GMT年1月1日以來的整數毫秒數，或是具有以下格式之一的日期/時間字串值：

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*： *`mm`*： *`ss`* GMT *`offset`*

*`hh`* 介於0到23之間。

*`zzz`* 是3或4個字元的時區代碼，例如&#39;GMT&#39;或&#39;PST&#39;。 以時區代碼說明日光節約時間。 例如，「PST」代表太平洋標準時間，「PDT」代表太平洋日光節約時間)。

*`offset`* 是時區時差（以小時為單位）或 `hours:minutes`，相對於GMT。 例如，「PDT」等於「GMT -7」。

字串格式日期/時間值的所有元素都必須存在。 如果日期/時間值的格式不正確，則會忽略該值並且其修改時間 `*`目錄`*.ini` 會改用檔案。

## 默认 {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` 如果欄位空白或不存在。

## 另请参阅 {#section-c42a427aa4794c548408dc4de028d578}

[attribute：：TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296)， [attribute：：UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8)， [attribute：：CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
