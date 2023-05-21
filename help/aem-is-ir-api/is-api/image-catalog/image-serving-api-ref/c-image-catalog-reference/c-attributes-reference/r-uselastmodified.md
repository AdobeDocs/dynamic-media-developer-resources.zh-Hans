---
description: 啟用上次修改的回應標頭。 啟用或停用在「影像伺服」發出的可快取HTTP回應中納入Last-Modified標頭。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

啟用上次修改的回應標頭。 啟用或停用在「影像伺服」發出的可快取HTTP回應中納入Last-Modified標頭。

伺服器使用最近的 `catalog::TimeStamp` 回應中涉及的所有目錄/目錄記錄的值，作為Last-Modified標頭值。

只有在使用的分散式快取網路或其他快取系統不支援etag標頭時，才應該啟用。

>[!NOTE]
>
>在涉及多個影像伺服主機的負載平衡環境中使用Last-Modified標頭時，務必謹慎。 如果伺服器出於某些原因對相同的目錄專案具有不同的時間戳記，可能會挫敗使用者端快取，並增加伺服器負載。 這種情況可能會發生，如下所示：
>
>* 兩者皆非 `catalog::TimeStamp` 也不 `attribute::TimeStamp`，如此一來， [!DNL catalog.ini] 檔案為的預設值 `catalog::TimeStamp`.
>
>* 每個伺服器在本機檔案系統上都有其自己的目錄檔案執行個體，而不是透過網路掛載來共用影像目錄檔案。
>* 兩個或多個相同的執行個體 [!DNL catalog.ini] 檔案的修改日期不同，可能是因為檔案複製不當所造成。
>


## 屬性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

标记. 0代表停用，1代表啟用Last-Modified HTTP標題。

## 默认 {#section-4eb47aadab8b41609bef296a4115f9f4}

繼承自 `default::UseLastModified` 如果未定義或為空。

## 另请参阅 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog：：TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
