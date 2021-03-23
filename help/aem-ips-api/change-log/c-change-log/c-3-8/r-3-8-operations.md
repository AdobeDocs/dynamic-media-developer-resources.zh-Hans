---
description: 介绍IPS API 3.8版的新操作方法和更改的操作方法。
seo-description: 介绍IPS API 3.8版的新操作方法和更改的操作方法。
seo-title: 操作新增和修改
solution: Experience Manager
title: 操作新增和修改
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---


# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API 3.8版的新操作方法和更改的操作方法。

语法

## 新操作{#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 修改后的操作{#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* 可选的`publishState`参数允许您搜索`MarkedForPublish/NotMarkedForPublish`资产状态。

**getJobLogs**

* 可选的`userHandle`参数允许您检索由特定用户提交的作业日志。

