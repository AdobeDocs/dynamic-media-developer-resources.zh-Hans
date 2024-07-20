---
description: 介绍IPS API版本3.8的新操作和更改的操作方法。
solution: Experience Manager
title: 新操作和修改后的操作
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本3.8的新操作和更改的操作方法。

语法

## 新操作 {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 已修改的操作 {#section-25eee732b69c49d0a27b1f3290f8654a}

**搜索资产**

* 可选的`publishState`参数允许您搜索`MarkedForPublish/NotMarkedForPublish`资源状态。

**getJobLogs**

* 可选的`userHandle`参数允许您检索特定用户提交的作业日志。
