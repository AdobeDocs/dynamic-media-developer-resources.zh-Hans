---
description: 說明IPS API 3.7版的新增和變更的作業方法。
solution: Experience Manager
title: 新作業和修改作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 6%

---

# 作業：新增與修改{#operations-new-and-modified}

說明IPS API 3.7版的新增和變更的作業方法。

语法

## 新作業 {#section-c4d34a58f8194d548fbe26ab3764ea58}

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

## 已修改的作業 {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* 已移除 `name` 引數。
* 增加了 `excludeFieldArray`.

**getFolders**

* 增加了 `excludeFieldArray`.

**getFolderTree**

* 已新增 `excludeFieldArray` 和 `getUniqueMetadataValues`.
* 已建立 `fieldHandle` 必要引數。
