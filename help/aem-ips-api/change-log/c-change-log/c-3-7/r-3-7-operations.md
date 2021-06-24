---
description: 介绍IPS API版本3.7的新操作方法和已更改的操作方法。
solution: Experience Manager
title: 操作（新增和修改）
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 5%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本3.7的新操作方法和已更改的操作方法。

语法

## 新操作 {#section-c4d34a58f8194d548fbe26ab3764ea58}

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

## 修改的操作 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* 删除了`name`参数。
* 增加了 `excludeFieldArray`.

**getFolders**

* 增加了 `excludeFieldArray`.

**getFolderTree**

* 添加了`excludeFieldArray`和`getUniqueMetadataValues`。
* 将`fieldHandle`设为必需参数。
