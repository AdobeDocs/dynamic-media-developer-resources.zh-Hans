---
description: 說明IPS API 4.2版的新資料和變更資料型別。
solution: Experience Manager
title: 新增和修改的資料型別
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 1%

---

# 資料型別：新增和修改{#data-types-new-and-modified}

說明IPS API 4.2版的新資料和變更資料型別。

语法

## 新型別 {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 修改型別 {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**資產**

引數已新增：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

引數已移除：

* `ImageSetInfo`
* `RenderSetInfo`

**重新處理資產工作**

引數已新增：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectory作業**

引數已新增：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

引數已新增：

* `preservePublishState`
* `preserveCrop`
