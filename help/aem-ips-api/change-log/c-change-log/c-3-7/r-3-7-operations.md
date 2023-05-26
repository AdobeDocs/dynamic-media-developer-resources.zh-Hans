---
description: 介绍IPS API版本3.7的新操作和更改的操作方法。
solution: Experience Manager
title: 新操作和修改后的操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 6%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本3.7的新操作和更改的操作方法。

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

## 已修改的操作 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* 已删除 `name` 参数。
* 增加了 `excludeFieldArray`.

**getFolders**

* 增加了 `excludeFieldArray`.

**getFolderTree**

* 已添加 `excludeFieldArray` 和 `getUniqueMetadataValues`.
* 已制作 `fieldHandle` 一个必需的参数。
