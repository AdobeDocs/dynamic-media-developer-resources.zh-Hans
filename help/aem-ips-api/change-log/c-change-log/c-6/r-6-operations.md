---
description: 介绍IPS API版本6的新操作和更改的操作方法。
solution: Experience Manager
title: 新操作和修改后的操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本6的新操作和更改的操作方法。

语法

## 新操作 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 已修改的操作 {#section-f4e8755527444266ae806e3f4c851ae6}

**增加了**

* 已添加 `isHidden` 和 `initialTagValue` 至：

   * `saveMetadataField`
   * ` `updateMetadataField
   * `createMetadataField`

* 已添加 `thumbAssetHandle` 至：

   * `createImageSet`
   * `createAssetSet`

   已添加 `companyHandle` 至：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   已添加 `contextHandle` 到：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* 已将includeInactive添加到：

   * `getUsers`.
   * `getUserChars`.

* 已添加 `permissionArray` 到 `createPropertySet`.

* 已添加 `exportJob` 到 `submitJob`.

**將**

* In `addUser` 和 `setUser`，已更改 `role` 到 `defaultRole`.

* In `getCompanyMembers`，已更改 `userArray` 到 `memberArray`.

* In `getCompanyMembership`，已更改 `companyArray` 到 `membershipArray`.

* In `addUser`， `setCompanyMembership`、和 `addCompanyMembership`，已更改 `membershipArray` 到 `companyHandleArray`.

* In `getCompanyMembership`，已更改 `companyArray` 到 `membershipArray`.

* In `getUserChars`， `includeInvalid` 现在是可选的。

**已删除**

* 已删除 `renameFiles` 起始日期 `renameAsset`.

* 已删除 `getXMPPanelViewDefinition`.
* 已删除 `searchAssetsByFulltext` 和 `searchAssetsBySimilarity`.
