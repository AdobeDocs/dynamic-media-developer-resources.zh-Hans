---
description: 介绍IPS API版本6的新操作和更改的操作方法。
solution: Experience Manager
title: 新操作和修改后的操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

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

**已添加**

* 已将`isHidden`和`initialTagValue`添加到：

   * `saveMetadataField`
   * ` `updateMetadataField”
   * `createMetadataField`

* 已将`thumbAssetHandle`添加到：

   * `createImageSet`
   * `createAssetSet`

  已将`companyHandle`添加到：

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  已将`contextHandle`添加到：

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* 已将includeInactive添加到：

   * `getUsers`.
   * `getUserChars`.

* 已将`permissionArray`添加到`createPropertySet`。

* 已将`exportJob`添加到`submitJob`。

**已更改**

* 在`addUser`和`setUser`中，将`role`更改为`defaultRole`。

* 在`getCompanyMembers`中，将`userArray`更改为`memberArray`。

* 在`getCompanyMembership`中，将`companyArray`更改为`membershipArray`。

* 在`addUser`、`setCompanyMembership`和`addCompanyMembership`中，将`membershipArray`更改为`companyHandleArray`。

* 在`getCompanyMembership`中，将`companyArray`更改为`membershipArray`。

* 在`getUserChars`中，`includeInvalid`现在为可选。

**已删除**

* 已从`renameFiles`中移除`renameAsset`。

* 已删除`getXMPPanelViewDefinition`。
* 已删除`searchAssetsByFulltext`和`searchAssetsBySimilarity`。
