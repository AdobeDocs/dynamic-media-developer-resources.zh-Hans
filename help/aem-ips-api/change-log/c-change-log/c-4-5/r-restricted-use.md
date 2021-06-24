---
description: 测试版WSDL中提供的这些新操作或修改操作和数据类型，在Dynamic Media开发的应用程序之外不使用。
solution: Experience Manager
title: 限制使用
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 限制使用{#restricted-use}

测试版WSDL中提供的这些新操作或修改操作和数据类型，在Dynamic Media开发的应用程序之外不使用。

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
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**修改的类型**

* 更改了`ActiveJob`以包含`createVideoSitemapJob`类型

* 更改了`ScheduledJob`以包含`createVideoSitemapJob`类型

* 更改了`ImageServingPublishJob`以包含可选的`contextHandle`

* 更改了`ImageRenderingPublishJob`以包含可选的`contextHandle`

* 更改了`MetadataField`以包含可选的`initialTagField`

* 将`MetadataCondition`更改为包含和可选`caseSensitive`参数

* 已将`PropertySet`更改为将可选`PermissionArray`包含为`permissions`

* 已将`UploadDirectoryJob`更改为包含可选`xmpKeywords`、`xmpTemplateId`和`xmpTemplateOverride`参数

* 更改了`VideoPublishJob`以包含可选的`contextHandle`

**修改的操作**

* 更改了`createAssetSet`以包含可选的`thumbAssetHandle`

* 更改了`createImageSet`以包含可选的`thumbAssetHandle`

* 更改了`createMetadataField`以包含可选的`initialTagValue`参数

* 已将`createPropertySet`更改为将可选`PermissionUpdateArray`包含为`permissionArray`

* 更改了`getImageServingPublishSettings`以包含可选的`contextHandle`参数

* 更改了`getImageRenderingPublishSettings`以包含可选的`contextHandle`参数

* 更改了`searchAssetsByFullText`以包含一系列可选参数：

   * `SearchFilter` 作为参 `filters` 数

   * `sortBy`
   * `sortDirection`

* 更改了`searchAssetsByMetadata`以包含一系列可选参数：

   * `SearchFilter` 作为参 `filters` 数

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` 七个参数序列

* 已将`setAssetPublishState`更改为将可选`HandleArray`包含为`contextHandleArray`

* 更改了`setImageServingPublishSettings`以包含可选的`contextHandle`参数

* 更改了`setImageRenderingPublishSettings`以包含可选`contextHandle`参数

* 更改了`submitJob`以包含可选`createVideoSitemap`作业类型
