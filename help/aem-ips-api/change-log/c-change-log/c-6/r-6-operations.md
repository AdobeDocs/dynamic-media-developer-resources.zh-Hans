---
description: 介绍IPS API版本6的新操作和更改的操作方法。
solution: Experience Manager
title: 新操作和修改后的操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
TQID: 'https://experienceleague.adobe.com/DLA26IsxxpZ0TSSfQBrvZSl8mbcJCaTfnpK-bhhmglg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
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

* 已从`renameAsset`中移除`renameFiles`。

* 已删除`getXMPPanelViewDefinition`。
* 已删除`searchAssetsByFulltext`和`searchAssetsBySimilarity`。
