---
description: 介绍IPS API版本4.5的新数据类型和已更改的数据类型。
solution: Experience Manager
title: 数据类型新建和修改
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 2%

---


# 数据类型：新建和已修改{#data-types-new-and-modified}

介绍IPS API版本4.5的新数据类型和已更改的数据类型。

语法

## 新类型{#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## 修改类型{#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 资产包含一个新的`fileName`字段，用于返回虚拟文件名。
* `AssetSummary` 返回 `type` 和字 `name` 段

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要并 `urlArray` 添加可选计 `numUrls` 数

