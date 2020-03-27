---
description: 介绍IPS API 3.8版的新操作方法和更改的操作方法。
seo-description: 介绍IPS API 3.8版的新操作方法和更改的操作方法。
seo-title: 操作（新增和修改）
solution: Experience Manager
title: 操作（新增和修改）
topic: Scene7 Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 操作：新增和已修改{#operations-new-and-modified}

介绍IPS API 3.8版的新操作方法和更改的操作方法。

语法

## 新操作 {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 修改后的操作 {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* 可选参 `publishState` 数允许您搜索资产 `MarkedForPublish/NotMarkedForPublish` 状态。

**getJobLogs**

* 可选参 `userHandle` 数允许您检索特定用户提交的作业日志。

