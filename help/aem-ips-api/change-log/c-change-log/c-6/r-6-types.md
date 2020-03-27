---
description: 介绍IPS API版本6的新类型和更改的类型。
seo-description: 介绍IPS API版本6的新类型和更改的类型。
seo-title: 数据类型新增和修改
solution: Experience Manager
title: 数据类型新增和修改
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 数据类型：新增和已修改{#data-types-new-and-modified}

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

## 修改类型 {#section-56b834b1a3b843279d8715b4a4f3890b}

**增加了**

* 已添 `numUrls` 加到 `UploadUrlsJob`。

* 添加到 `fileName``Asset.`

* 已添 `isHidden` 加到 `MetadataField`。

* 已添 `taskState` 加到 `TaskProgress`。

* 添加到 `exportJob` 和 `ActiveJob` 中 `ScheduledJob`。

* 已 `optmizedPath` 添加 `optimizedFile` 和 `PsdInfo`。

* 已添 `contextHandle` 加到：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 将以下参数添加到 `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**將**

* 在 `User`中， `role` 更改为 `defaultRole`。

* 在 `Folder`中， `permissions` 更改为 `permissionsSetHandle`。

* In `AssetSummary`和 `type` 现 `name` 在是可选的。

