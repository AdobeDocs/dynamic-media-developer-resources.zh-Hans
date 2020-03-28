---
description: 测试版WSDL中提供的这些新操作或修改操作和数据类型不可在Scene7开发的应用程序之外使用。
seo-description: 测试版WSDL中提供的这些新操作或修改操作和数据类型不可在Scene7开发的应用程序之外使用。
seo-title: 限制使用
solution: Experience Manager
title: 限制使用
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 限制使用{#restricted-use}

测试版WSDL中提供的这些新操作或修改操作和数据类型不可在Scene7开发的应用程序之外使用。

这些操作和类型可能会在后续系统更新中禁用、更改或弃用。

**新类型**

* AssetPublishContexts
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**新操作**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimiliary
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**修改类型**

* 更改 `ActiveJob` 为包含类 `createVideoSitemapJob` 型

* 更改 `ScheduledJob` 为包含类 `createVideoSitemapJob` 型

* 更改 `ImageServingPublishJob` 为包含可选 `contextHandle`

* 更改 `ImageRenderingPublishJob` 为包含可选 `contextHandle`

* 更改 `MetadataField` 为包含可选 `initialTagField`

* 更改 `MetadataCondition` 为包含和可选参 `caseSensitive` 数

* 更改 `PropertySet``PermissionArray` 为将可选项包含为 `permissions`

* 更改 `UploadDirectoryJob` 为包括可选 `xmpKeywords`参数 `xmpTemplateId` 和参 `xmpTemplateOverride` 数

* 更改 `VideoPublishJob` 为包含可选 `contextHandle`

**修改后的操作**

* 更改 `createAssetSet` 为包含可选 `thumbAssetHandle`

* 更改 `createImageSet` 为包含可选 `thumbAssetHandle`

* 更改 `createMetadataField` 为包含可选参 `initialTagValue` 数

* 更改 `createPropertySet``PermissionUpdateArray` 为将可选项包含为 `permissionArray`

* 更改 `getImageServingPublishSettings` 为包含可选参 `contextHandle` 数

* 更改 `getImageRenderingPublishSettings` 为包含可选参 `contextHandle` 数

* 更改 `searchAssetsByFullText` 为包括一系列可选参数：

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`

* 更改 `searchAssetsByMetadata` 为包括一系列可选参数：

   * `SearchFilter` as `filters` parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 七个参数序列

* 更改 `setAssetPublishState``HandleArray` 为将可选项包含为 `contextHandleArray`

* 更改 `setImageServingPublishSettings` 为包含可选参 `contextHandle` 数

* 更改 `setImageRenderingPublishSettings` 为包含可选参 `contextHandle`数

* 已更 `submitJob` 改为包含可选作 `createVideoSitemap` 业类型

