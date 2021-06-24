---
description: 介绍IPS API版本4.5的新数据类型和已更改的数据类型。
solution: Experience Manager
title: 数据类型新增和修改
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# 数据类型：新建和已修改{#data-types-new-and-modified}

介绍IPS API版本4.5的新数据类型和已更改的数据类型。

语法

## 新类型 {#section-6941b228cf6747a987e98c3d6e4b6b17}

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

## 修改的类型 {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 资产包含一个新的`fileName`字段，用于返回虚拟文件名。
* `AssetSummary` 返回 `type` 和字 `name` 段

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要 `urlArray` 并添加可选计 `numUrls` 数
