---
description: 介绍IPS API版本6的新操作方法和更改的操作方法。
seo-description: 介绍IPS API版本6的新操作方法和更改的操作方法。
seo-title: 操作（新增和修改）
solution: Experience Manager
title: 操作（新增和修改）
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 操作：新增和已修改{#operations-new-and-modified}

介绍IPS API版本6的新操作方法和更改的操作方法。

语法

## 新操作 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 修改后的操作 {#section-f4e8755527444266ae806e3f4c851ae6}

**增加了**

* 已添 `isHidden` 加和 `initialTagValue` 添加到：

   * `saveMetadataField`
   * ` `updateMetadataField”
   * `createMetadataField`

* 已添 `thumbAssetHandle` 加到：

   * `createImageSet`
   * `createAssetSet`
   已添 `companyHandle` 加到：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   已添 `contextHandle` 加到：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* 将includeInactive添加到：

   * `getUsers`.
   * `getUserChars`.

* 已添 `permissionArray` 加到 `createPropertySet`。

* 已添 `exportJob` 加到 `submitJob`。

**將**

* 在 `addUser` 和 `setUser`中，更 `role` 改为 `defaultRole`。

* 在 `getCompanyMembers`中， `userArray` 更改为 `memberArray`。

* 在 `getCompanyMembership`中， `companyArray` 更改为 `membershipArray`。

* In `addUser`、 `setCompanyMembership`和 `addCompanyMembership`，已更 `membershipArray` 改为 `companyHandleArray`。

* 在 `getCompanyMembership`中， `companyArray` 更改为 `membershipArray`。

* 在 `getUserChars`中， `includeInvalid` 现在为可选。

**已删除**

* 已从 `renameFiles` 中删除 `renameAsset`。

* 已删除 `getXMPPanelViewDefinition`.
* 已删 `searchAssetsByFulltext` 除和 `searchAssetsBySimilarity`。

