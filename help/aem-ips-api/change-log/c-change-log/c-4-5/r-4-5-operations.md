---
description: 介绍IPS API版本4.5的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新增和修改
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本4.5的新操作方法和更改的操作方法。

语法

## 新操作{#section-a3be679d8e9345aba2e97699c3a537b9}

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

## 修改后的操作{#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 包括 `animatedGifInfo`、 `swcInfo`、 `cssInfo`和 `javascriptInfo` 参数。

* `createMetadataField` 包括可选 `isHidden` 参数。

* `saveMetadataField` 包括可选 `isHidden` 参数。

* `searchAssets`
* 
* `renameFiles`参数已在先前版本中弃用，并已从`renameAsset`操作中删除。 虚拟文件路径将更改为与新资源名称（保留文件扩展名）匹配，而物理文件路径不受影响。 API客户端在更新到新API版本时需要删除对此参数的引用。

