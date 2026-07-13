---
description: 介绍IPS API版本3.7的新操作和更改的操作方法。
solution: Experience Manager
title: 新操作和修改后的操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
TQID: 'https://experienceleague.adobe.com/nt-KwoxJw8bSbt076MIIZlXW2YbMzwVURLwE-94hlDU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 50
ht-degree: 2%

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

**搜索资产**

* 删除了`name`参数。
* 已添加`excludeFieldArray`。

**getFolders**

* 已添加`excludeFieldArray`。

**getFolderTree**

* 已添加`excludeFieldArray`和`getUniqueMetadataValues`。
* 将`fieldHandle`设为必需参数。

