---
description: 說明IPS API 4.5版的新增和變更的作業方法。
solution: Experience Manager
title: 作業 — 新增與修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# 作業：新增與修改{#operations-new-and-modified}

說明IPS API 4.5版的新增和變更的作業方法。

语法

## 新作業 {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## 已修改的作業 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 包含 `animatedGifInfo`， `swcInfo`， `cssInfo`、和 `javascriptInfo` 引數。
* `createMetadataField` 包含選購專案 `isHidden` 引數。
* `saveMetadataField` 包含選購專案 `isHidden` 引數。
* `searchAssets`
* 此 `renameFiles` 舊版已棄用引數，並已從 `renameAsset` 作業。 虛擬檔案路徑會變更為符合新的資產名稱（保留副檔名），而實體檔案路徑則不受影響。 API使用者端在更新至新API版本時需要移除此引數的參考。
