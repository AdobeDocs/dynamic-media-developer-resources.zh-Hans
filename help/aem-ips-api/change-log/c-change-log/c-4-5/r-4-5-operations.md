---
description: 介绍IPS API版本4.5的新操作方法和已更改的操作方法。
seo-description: 介绍IPS API版本4.5的新操作方法和已更改的操作方法。
seo-title: 操作新增和修改
solution: Experience Manager
title: 操作新增和修改
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本4.5的新操作方法和已更改的操作方法。

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

* `Asset` 包括 `animatedGifInfo`、 `swcInfo`、 `cssInfo`和参 `javascriptInfo` 数。

* `createMetadataField` 包括可选 `isHidden` 参数。

* `saveMetadataField` 包括可选 `isHidden` 参数。

* `searchAssets`
* 
* `renameFiles`参数已在先前发行版中弃用，并从`renameAsset`操作中删除。 虚拟文件路径会更改为与新资产名称（保留文件扩展名）匹配，而物理文件路径则不受影响。 API客户端在更新到新API版本时需要删除对此参数的引用。

