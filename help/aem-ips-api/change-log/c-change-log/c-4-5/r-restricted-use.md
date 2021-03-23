---
description: 测试版WSDL中提供的这些新操作或修改操作和数据类型在Dynamic Media开发的应用程序之外不可使用。
solution: Experience Manager
title: 受限使用
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# 受限用途{#restricted-use}

测试版WSDL中提供的这些新操作或修改操作和数据类型在Dynamic Media开发的应用程序之外不可使用。

这些操作和类型可能会在后续系统更新中禁用、更改或停用。

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

**修改的类型**

* 将`ActiveJob`更改为包含`createVideoSitemapJob`类型

* 将`ScheduledJob`更改为包含`createVideoSitemapJob`类型

* 将`ImageServingPublishJob`更改为包含可选`contextHandle`

* 将`ImageRenderingPublishJob`更改为包含可选`contextHandle`

* 将`MetadataField`更改为包含可选`initialTagField`

* 已将`MetadataCondition`更改为包含和可选`caseSensitive`参数

* 将`PropertySet`更改为将可选`PermissionArray`包含为`permissions`

* 将`UploadDirectoryJob`更改为包含可选`xmpKeywords`、`xmpTemplateId`和`xmpTemplateOverride`参数

* 将`VideoPublishJob`更改为包含可选`contextHandle`

**修改的操作**

* 将`createAssetSet`更改为包含可选`thumbAssetHandle`

* 将`createImageSet`更改为包含可选`thumbAssetHandle`

* 将`createMetadataField`更改为包含可选`initialTagValue`参数

* 将`createPropertySet`更改为将可选`PermissionUpdateArray`包含为`permissionArray`

* 将`getImageServingPublishSettings`更改为包含可选`contextHandle`参数

* 将`getImageRenderingPublishSettings`更改为包含可选`contextHandle`参数

* 更改`searchAssetsByFullText`以包含一系列可选参数：

   * `SearchFilter` as参 `filters` 数

   * `sortBy`
   * `sortDirection`

* 更改`searchAssetsByMetadata`以包含一系列可选参数：

   * `SearchFilter` as参 `filters` 数

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 七个参数序列

* 将`setAssetPublishState`更改为将可选`HandleArray`包含为`contextHandleArray`

* 将`setImageServingPublishSettings`更改为包含可选`contextHandle`参数

* 将`setImageRenderingPublishSettings`更改为包含可选`contextHandle`参数

* 将`submitJob`更改为包含可选`createVideoSitemap`作业类型

