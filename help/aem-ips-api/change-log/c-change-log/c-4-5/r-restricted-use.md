---
description: 测试版WSDL中提供的这些新的或修改后的操作和数据类型不得在Dynamic Media开发的应用程序之外使用。
solution: Experience Manager
title: 限制使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 限制使用{#restricted-use}

测试版WSDL中提供的这些新的或修改后的操作和数据类型不得在Dynamic Media开发的应用程序之外使用。

这些操作和类型可能会因后续系统更新而禁用、更改或弃用。

**新类型**

* AssetPublishContext
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* Publishcontext
* PublishContextArray
* SearchFilter
* 长数组

**新操作**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContext
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAsset
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**已修改类型**

* 已更改 `ActiveJob` 以包含 `createVideoSitemapJob` type

* 已更改 `ScheduledJob` 以包含 `createVideoSitemapJob` type

* 已更改 `ImageServingPublishJob` 以包含可选 `contextHandle`

* 已更改 `ImageRenderingPublishJob` 以包含可选 `contextHandle`

* 已更改 `MetadataField` 以包含可选 `initialTagField`

* 已更改 `MetadataCondition` 要包含的和可选 `caseSensitive` 参数

* 已更改 `PropertySet` 以包含可选 `PermissionArray` 作为 `permissions`

* 已更改 `UploadDirectoryJob` 要包括可选内容，请执行以下操作 `xmpKeywords`， `xmpTemplateId` 和 `xmpTemplateOverride` 参数

* 已更改 `VideoPublishJob` 以包含可选 `contextHandle`

**已修改的操作**

* 已更改 `createAssetSet` 以包含可选 `thumbAssetHandle`

* 已更改 `createImageSet` 以包含可选 `thumbAssetHandle`

* 已更改 `createMetadataField` 以包含可选 `initialTagValue` 参数

* 已更改 `createPropertySet` 以包含可选 `PermissionUpdateArray` 作为 `permissionArray`

* 已更改 `getImageServingPublishSettings` 以包含可选 `contextHandle` 参数

* 已更改 `getImageRenderingPublishSettings` 以包含可选 `contextHandle` 参数

* 已更改 `searchAssetsByFullText` 要包含一系列可选参数，请执行以下操作：

   * `SearchFilter` 作为 `filters` 参数

   * `sortBy`
   * `sortDirection`

* 已更改 `searchAssetsByMetadata` 要包含一系列可选参数，请执行以下操作：

   * `SearchFilter` 作为 `filters` 参数

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 7个参数的序列

* 已更改 `setAssetPublishState` 以包含可选 `HandleArray` 作为 `contextHandleArray`

* 已更改 `setImageServingPublishSettings` 以包含可选 `contextHandle` 参数

* 已更改 `setImageRenderingPublishSettings` 以包含可选 `contextHandle`参数

* 已更改 `submitJob` 以包含可选 `createVideoSitemap` 作业类型
