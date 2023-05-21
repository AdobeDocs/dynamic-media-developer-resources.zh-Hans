---
description: 使用目錄型或過期型快取驗證來自動重新整理快取專案，如使用屬性CacheValidationPolicy （在default.ini或特定影像目錄的.ini檔案中）所選取。
solution: Experience Manager
title: 回應快取驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 回應快取驗證{#response-cache-validation}

使用目錄型或過期型快取驗證來自動重新整理快取專案，如使用attribute：：CacheValidationPolicy （在default.ini或特定影像目錄的.ini檔案中）所選取。

若使用目錄型驗證，則現有的快取專案會被視為過時 `catalog::LastModified` (或 `attribute::LastModified`，或的檔案修改時間 [!DNL catalog.ini] file)的時間比建立快取專案的時間更近。

使用過期基準驗證，快取專案在距最近一次驗證後5分鐘後會過時。 在這兩種情況下，伺服器會檢查與建立請求有關的所有影像檔案的檔案日期，以驗證過時的快取專案。 如果檔案日期未變更，則會更新快取專案的時間戳記，並將快取日期視為有效。

對於主要涉及在影像目錄中註冊的影像的典型應用程式，目錄型驗證可提供效能優勢。 不涉及影像目錄的應用程式應使用過期快取驗證。 達成此目標的一種方式是設定 `attribute::cacheValidationPolicy=0` 在 [!DNL default.ini]，並至 `1` 於所有特定影像目錄檔案中。

當請求中涉及的目錄專案以可能導致回覆影像變更的方式變更時，快取專案會變成無效並需要重新產生。 例如， `catalog::Modifier` 變更。

>[!NOTE]
>
>Dynamic Media金字塔TIFF(PTIFF)影像會在檔案標題內部維護檔案日期，以用於驗證。 檔案系統維護的檔案修改時間用於檢查非PTIFF檔案是否已變更。

只有影像檔案會參與快取驗證程式。 變更字型檔案或ICC設定檔檔案不會造成快取專案自動失效。
