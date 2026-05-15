---
description: 测试版WSDL中提供的这些新操作或修改后的操作和数据类型不得在Dynamic Media开发的应用程序之外使用。
solution: Experience Manager
title: 限制使用
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
TQID: 'https://experienceleague.adobe.com/X-Q28iVTM95SDSwlSy3yhmJcfJv0TC3LtxXPRv8RCpg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 限制使用{#restricted-use}

测试版WSDL中提供的这些新操作或修改后的操作和数据类型不得在Dynamic Media开发的应用程序之外使用。

这些操作和类型可能会因为后续的系统更新而被禁用、更改或弃用。

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
* 更新图像集
* updatePropertySetPermissions

**修改的类型**

* 已更改`ActiveJob`以包含`createVideoSitemapJob`类型

* 已更改`ScheduledJob`以包含`createVideoSitemapJob`类型

* 已更改`ImageServingPublishJob`以包含可选`contextHandle`

* 已更改`ImageRenderingPublishJob`以包含可选`contextHandle`

* 已更改`MetadataField`以包含可选`initialTagField`

* 已将`MetadataCondition`更改为包含和可选`caseSensitive`参数

* 已更改`PropertySet`以包含可选的`PermissionArray`作为`permissions`

* 已更改`UploadDirectoryJob`以包含可选的`xmpKeywords`、`xmpTemplateId`和`xmpTemplateOverride`参数

* 已更改`VideoPublishJob`以包含可选`contextHandle`

**已修改的操作**

* 已更改`createAssetSet`以包含可选`thumbAssetHandle`

* 已更改`createImageSet`以包含可选`thumbAssetHandle`

* 已更改`createMetadataField`以包含可选的`initialTagValue`参数

* 已更改`createPropertySet`以包含可选的`PermissionUpdateArray`作为`permissionArray`

* 已更改`getImageServingPublishSettings`以包含可选的`contextHandle`参数

* 已更改`getImageRenderingPublishSettings`以包含可选的`contextHandle`参数

* 已更改`searchAssetsByFullText`以包含一系列可选参数：

   * `SearchFilter`作为`filters`参数

   * `sortBy`
   * `sortDirection`

* 已更改`searchAssetsByMetadata`以包含一系列可选参数：

   * `SearchFilter`作为`filters`参数

   * `sortBy`
   * `sortDirection`
   * 七个参数的`haystackSearch`序列

* 已更改`setAssetPublishState`以包含可选的`HandleArray`作为`contextHandleArray`

* 已更改`setImageServingPublishSettings`以包含可选的`contextHandle`参数

* 已更改`setImageRenderingPublishSettings`以包含可选的`contextHandle`参数

* 已更改`submitJob`以包含可选的`createVideoSitemap`作业类型
