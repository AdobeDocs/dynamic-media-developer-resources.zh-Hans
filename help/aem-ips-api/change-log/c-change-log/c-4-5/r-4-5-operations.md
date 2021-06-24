---
description: 介绍IPS API版本4.5的新操作方法和已更改的操作方法。
solution: Experience Manager
title: 操作（新增和修改）
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本4.5的新操作方法和已更改的操作方法。

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

## 修改的操作 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 包括 `animatedGifInfo`、 `swcInfo`、 `cssInfo`和参 `javascriptInfo` 数。

* `createMetadataField` 包含可选 `isHidden` 参数。

* `saveMetadataField` 包含可选 `isHidden` 参数。

* `searchAssets`
* 
* 以前版本已弃用`renameFiles`参数，并从`renameAsset`操作中删除了该参数。 虚拟文件路径会进行更改以匹配新资产名称（保留文件扩展名），而物理文件路径则不会受到影响。 API客户端在更新到新API版本时，需要删除对此参数的引用。
