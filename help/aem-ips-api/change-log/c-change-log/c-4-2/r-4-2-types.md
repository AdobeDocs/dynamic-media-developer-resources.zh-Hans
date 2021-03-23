---
description: 介绍IPS API版本4.2的新数据类型和已更改的数据类型。
solution: Experience Manager
title: 数据类型新建和修改
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 3%

---


# 数据类型：新建和已修改{#data-types-new-and-modified}

介绍IPS API版本4.2的新数据类型和已更改的数据类型。

语法

## 新类型{#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## 修改类型{#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**资源**

添加的参数：

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

删除的参数：

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

添加的参数：

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

添加的参数：

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

添加的参数：

* `preservePublishState`
* `preserveCrop`

