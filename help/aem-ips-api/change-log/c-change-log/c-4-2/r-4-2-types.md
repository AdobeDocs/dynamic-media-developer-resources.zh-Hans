---
description: 介绍IPS API版本4.2的新数据类型和已更改的数据类型。
solution: Experience Manager
title: 数据类型新增和修改
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 3%

---

# 数据类型：新建和已修改{#data-types-new-and-modified}

介绍IPS API版本4.2的新数据类型和已更改的数据类型。

语法

## 新类型 {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 修改的类型 {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**资源**

添加了以下参数：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

删除的参数：

* `ImageSetInfo`
* `RenderSetInfo`

**重新处理AssetsJob**

添加了以下参数：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

添加了以下参数：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

添加了以下参数：

* `preservePublishState`
* `preserveCrop`
