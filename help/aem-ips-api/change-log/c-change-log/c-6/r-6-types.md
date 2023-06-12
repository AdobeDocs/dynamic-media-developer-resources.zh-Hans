---
description: 介绍IPS API版本6的新类型和更改类型。
solution: Experience Manager
title: 新数据类型和修改的数据类型
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

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

**增加了**

* 已添加 `numUrls` 到 `UploadUrlsJob`.

* 已添加 `fileName` 到 `Asset.`

* 已添加 `isHidden` 到 `MetadataField`.

* 已添加 `taskState` 到 `TaskProgress`.

* 已添加 `exportJob` 到 `ActiveJob` 和 `ScheduledJob`.

* 已添加 `optmizedPath` 和 `optimizedFile` 到 `PsdInfo`.

* 已添加 `contextHandle` 到：

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* 已将以下参数添加到 `Asset`：

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**將**

* In `User`，已更改 `role` 到 `defaultRole`.

* In `Folder`，已更改 `permissions` 到 `permissionsSetHandle`.

* In `AssetSummary`， `type` 和 `name` 现在是可选的。
