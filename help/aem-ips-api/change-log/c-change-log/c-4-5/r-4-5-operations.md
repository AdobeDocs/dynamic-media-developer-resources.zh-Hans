---
description: 介绍IPS API版本4.5的新操作和更改的操作方法。
solution: Experience Manager
title: 操作 — 新建和已修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本4.5的新操作和更改的操作方法。

语法

## 新操作 {#section-a3be679d8e9345aba2e97699c3a537b9}

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

## 已修改的操作 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 包含 `animatedGifInfo`， `swcInfo`， `cssInfo`、和 `javascriptInfo` 参数。
* `createMetadataField` 包含一个可选 `isHidden` 参数。
* `saveMetadataField` 包含一个可选 `isHidden` 参数。
* `searchAssets`
* 此 `renameFiles` 参数在以前的版本中已弃用，已从 `renameAsset` 操作。 虚拟文件路径将更改以匹配新的资源名称（保留文件扩展名），而物理文件路径不受影响。 在更新到新的API版本时，API客户端需要移除对此参数的引用。
