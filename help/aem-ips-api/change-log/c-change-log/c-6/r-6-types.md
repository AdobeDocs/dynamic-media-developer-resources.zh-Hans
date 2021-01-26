---
description: 介绍IPS API版本6的新类型和更改的类型。
solution: Experience Manager
title: 数据类型新增和修改
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---


# 数据类型：新建和已修改{#data-types-new-and-modified}

介绍IPS API版本6的新类型和更改的类型。

语法

## 新类型{#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## 修改类型{#section-56b834b1a3b843279d8715b4a4f3890b}

**增加了**

* 将`numUrls`添加到`UploadUrlsJob`。

* 将`fileName`添加到`Asset.`

* 将`isHidden`添加到`MetadataField`。

* 将`taskState`添加到`TaskProgress`。

* 将`exportJob`添加到`ActiveJob`和`ScheduledJob`。

* 将`optmizedPath`和`optimizedFile`添加到`PsdInfo`。

* 已将`contextHandle`添加到：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 将以下参数添加到`Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**將**

* 在`User`中，将`role`更改为`defaultRole`。

* 在`Folder`中，将`permissions`更改为`permissionsSetHandle`。

* 在`AssetSummary`中，`type`和`name`现在是可选的。

