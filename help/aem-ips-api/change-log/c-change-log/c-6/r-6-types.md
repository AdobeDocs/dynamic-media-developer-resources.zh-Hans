---
description: 介绍IPS API版本6的新类型和更改类型。
solution: Experience Manager
title: 新增和修改的数据类型
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

---

# 数据类型：新增和已修改{#data-types-new-and-modified}

介绍IPS API版本6的新类型和更改类型。

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

## 已修改类型 {#section-56b834b1a3b843279d8715b4a4f3890b}

**已添加**

* 已将`numUrls`添加到`UploadUrlsJob`。

* 已将`fileName`添加到`Asset.`

* 已将`isHidden`添加到`MetadataField`。

* 已将`taskState`添加到`TaskProgress`。

* 已将`exportJob`添加到`ActiveJob`和`ScheduledJob`。

* 已将`optmizedPath`和`optimizedFile`添加到`PsdInfo`。

* 已将`contextHandle`添加到：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 已将以下参数添加到`Asset`：

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**已更改**

* 在`User`中，将`role`更改为`defaultRole`。

* 在`Folder`中，将`permissions`更改为`permissionsSetHandle`。

* 在`AssetSummary`中，`type`和`name`现在是可选的。
