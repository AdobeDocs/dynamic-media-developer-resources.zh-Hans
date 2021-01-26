---
description: 介绍IPS API 3.7版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新增和修改
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 6%

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

