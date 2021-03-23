---
description: 介绍IPS API 3.7版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新增和修改
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 5%

---


# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API 3.7版的新操作方法和更改的操作方法。

语法

## 新操作{#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## 修改后的操作{#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* 已删除`name`参数。
* 增加了 `excludeFieldArray`.

**getFolders**

* 增加了 `excludeFieldArray`.

**getFolderTree**

* 添加了`excludeFieldArray`和`getUniqueMetadataValues`。
* 使`fieldHandle`成为必需参数。

