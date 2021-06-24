---
description: 介绍IPS API版本6的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作（新增和修改）
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本6的新操作方法和更改的操作方法。

语法

## 新操作 {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 修改的操作 {#section-f4e8755527444266ae806e3f4c851ae6}

**增加了**

* 已将`isHidden`和`initialTagValue`添加到：

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
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

**將**

* 在`addUser`和`setUser`中，将`role`更改为`defaultRole`。

* 在`getCompanyMembers`中，将`userArray`更改为`memberArray`。

* 在`getCompanyMembership`中，将`companyArray`更改为`membershipArray`。

* 在`addUser`、`setCompanyMembership`和`addCompanyMembership`中，将`membershipArray`更改为`companyHandleArray`。

* 在`getCompanyMembership`中，将`companyArray`更改为`membershipArray`。

* 在`getUserChars`中，`includeInvalid`现在是可选的。

**已删除**

* 从`renameAsset`中删除了`renameFiles`。

* 已删除 `getXMPPanelViewDefinition`.
* 删除了`searchAssetsByFulltext`和`searchAssetsBySimilarity`。
