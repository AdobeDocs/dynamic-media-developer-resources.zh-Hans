---
description: 說明IPS API 3.8版的新增和變更的作業方法。
solution: Experience Manager
title: 新作業和修改作業
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---

# 作業：新增與修改{#operations-new-and-modified}

說明IPS API 3.8版的新增和變更的作業方法。

语法

## 新作業 {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## 已修改的作業 {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* 選填 `publishState` 引數可讓您搜尋 `MarkedForPublish/NotMarkedForPublish` 資產狀態。

**getJobLogs**

* 選填 `userHandle` 引數可讓您擷取特定使用者提交的工作記錄檔。
