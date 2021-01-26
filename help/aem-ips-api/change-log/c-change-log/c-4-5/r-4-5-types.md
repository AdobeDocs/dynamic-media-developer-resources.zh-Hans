---
description: 介绍IPS API版本4.5的新数据类型和已更改的数据类型。
solution: Experience Manager
title: 数据类型新增和修改
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

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

* 资产包含返回虚拟文件名的新`fileName`字段。
* `AssetSummary` 返回 `type` 和字 `name` 段

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要并 `urlArray` 添加可选计 `numUrls` 数

