---
description: 介绍IPS API版本6的新操作方法和更改的操作方法。
seo-description: 介绍IPS API版本6的新操作方法和更改的操作方法。
seo-title: 操作新增和修改
solution: Experience Manager
title: 操作新增和修改
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 5%

---


# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本6的新操作方法和更改的操作方法。

语法

## 新操作{#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## 修改后的操作{#section-f4e8755527444266ae806e3f4c851ae6}

**增加了**

* 将`isHidden`和`initialTagValue`添加到：

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



* 将includeInactive添加到：

   * `getUsers`.
   * `getUserChars`.

* 将`permissionArray`添加到`createPropertySet`。

* 将`exportJob`添加到`submitJob`。

**將**

* 在`addUser`和`setUser`中，将`role`更改为`defaultRole`。

* 在`getCompanyMembers`中，将`userArray`更改为`memberArray`。

* 在`getCompanyMembership`中，将`companyArray`更改为`membershipArray`。

* 在`addUser`、`setCompanyMembership`和`addCompanyMembership`中，将`membershipArray`更改为`companyHandleArray`。

* 在`getCompanyMembership`中，将`companyArray`更改为`membershipArray`。

* 在`getUserChars`中，`includeInvalid`现在是可选的。

**已删除**

* 已从`renameAsset`删除`renameFiles`。

* 已删除 `getXMPPanelViewDefinition`.
* 已删除`searchAssetsByFulltext`和`searchAssetsBySimilarity`。

