---
description: 介绍IPS API 3.8版的新操作方法和更改的操作方法。
solution: Experience Manager
title: 操作新增和修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '67'
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
