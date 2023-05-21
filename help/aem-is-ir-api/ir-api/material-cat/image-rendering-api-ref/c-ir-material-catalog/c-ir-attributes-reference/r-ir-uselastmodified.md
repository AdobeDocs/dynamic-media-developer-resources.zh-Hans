---
title: UseLastModified
description: 啟用上次修改的回應標頭。 啟用或停用在影像演算發出的可快取HTTP回應中包含Last-Modified標頭。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

啟用上次修改的回應標頭。 啟用或停用在影像演算發出的可快取HTTP回應中包含Last-Modified標頭。

伺服器使用最近的 `vignette::TimeStamp` 和 `catalog::TimeStamp` 回應中涉及的所有暈映和材質目錄/目錄記錄的值，作為Last-Modified標頭值。

只有在使用的分散式快取網路（例如Akamai）不支援etag標題時，才應啟用。

>[!NOTE]
>
>在涉及多個影像提供/轉譯主機的負載平衡環境中使用Last-Modified標頭時，必須謹慎。 如果伺服器出於某些原因對相同的目錄專案具有不同的時間戳記，可能會挫敗使用者端快取，並增加伺服器負載。 這種情況可能會發生，如下所示：

* `catalog::TimeStamp`， `vignette::TimeStamp`，或 `attribute::TimeStamp` 未定義，因此的修改時間 [!DNL catalog.ini] 檔案為的預設值 `catalog::TimeStamp`.

* 每個伺服器在本機檔案系統上都有其自己的目錄檔案執行個體，而不是透過網路掛載來共用素材目錄檔案。
* 兩個或多個相同的執行個體 [!DNL catalog.ini] 檔案的修改日期不同，可能是因為檔案複製不當所造成。

## 屬性 {#section-453952244193452caccfaf7f601007c1}

标记. 0代表停用，1代表啟用Last-Modified HTTP標題。

## 默认 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

繼承自 `default::UseLastModified` 如果未定義或為空。

## 另请参阅 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ， [暈映：：TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
