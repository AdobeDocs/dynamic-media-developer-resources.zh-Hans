---
description: 介绍IPS API版本6的新类型和更改的类型。
solution: Experience Manager
title: 数据类型新增和修改
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# 数据类型：新建和已修改{#data-types-new-and-modified}

介绍IPS API版本6的新类型和更改的类型。

语法

## 新类型 {#section-71ba6954339e4ba899acdf8a3212d6f3}

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

## 修改的类型 {#section-56b834b1a3b843279d8715b4a4f3890b}

**增加了**

* 已将`numUrls`添加到`UploadUrlsJob`。

* 已将`fileName`添加到`Asset.`

* 已将`isHidden`添加到`MetadataField`。

* 已将`taskState`添加到`TaskProgress`。

* 将`exportJob`添加到`ActiveJob`和`ScheduledJob`。

* 将`optmizedPath`和`optimizedFile`添加到`PsdInfo`。

* 已将`contextHandle`添加到：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 向`Asset`添加了以下参数：

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**將**

* 在`User`中，将`role`更改为`defaultRole`。

* 在`Folder`中，将`permissions`更改为`permissionsSetHandle`。

* 在`AssetSummary`中，`type`和`name`现在是可选的。
